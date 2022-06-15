## Basic access authentication
 basic access authentication is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request.

## Features

HTTP Basic authentication (BA) implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages; rather, HTTP Basic authentication uses standard fields in the HTTP header.

## Security

The BA mechanism does not provide confidentiality protection for the transmitted credentials. They are merely encoded with Base64 in transit and not encrypted or hashed in any way. Therefore, basic authentication is typically used in conjunction with HTTPS to provide confidentiality.

Because the BA field has to be sent in the header of each HTTP request, the web browser needs to cache credentials for a reasonable period of time to avoid constantly prompting the user for their username and password. Caching policy differs between browsers.

HTTP does not provide a method for a web server to instruct the client to "log out" the user. However, there are a number of methods to clear cached credentials in certain web browsers. One of them is redirecting the user to a URL on the same domain, using credentials that are intentionally incorrect. However, this behavior is inconsistent between various browsers and browser versions.[3] Microsoft Internet Explorer offers a dedicated JavaScript method to clear cached credentials:[4]

<script>document.execCommand('ClearAuthenticationCache');</script>
In modern browsers, cached credentials for basic authentication are typically cleared when clearing browsing history. Most browsers allow users to specifically clear only credentials, though the option may be hard to find, and typically clears credentials for all visited sites.[5][6]

## Protocol

Server side
When the server wants the user agent to authenticate itself towards the server after receiving an unauthenticated request, it must send a response with a HTTP 401 Unauthorized status line[7] and a WWW-Authenticate header field.[8]

The WWW-Authenticate header field for basic authentication is constructed as following:

WWW-Authenticate: Basic realm="User Visible Realm"

The server may choose to include the charset parameter from RFC 7617:[3]

WWW-Authenticate: Basic realm="User Visible Realm", charset="UTF-8"

This parameter indicates that the server expects the client to use UTF-8 for encoding username and password (see below).

## Client side

When the user agent wants to send authentication credentials to the server, it may use the Authorization header field.

The Authorization header field is constructed as follows:

The username and password are combined with a single colon (:). This means that the username itself cannot contain a colon.
The resulting string is encoded into an octet sequence. The character set to use for this encoding is by default unspecified, as long as it is compatible with US-ASCII, but the server may suggest use of UTF-8 by sending the charset parameter.
The resulting string is encoded using a variant of Base64 (+/ and with padding).
The authorization method and a space (e.g. "Basic ") is then prepended to the encoded string.
For example, if the browser uses Aladdin as the username and open sesame as the password, then the field's value is the Base64 encoding of Aladdin:open sesame, or QWxhZGRpbjpvcGVuIHNlc2FtZQ==. Then the Authorization header field will appear as:

Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==