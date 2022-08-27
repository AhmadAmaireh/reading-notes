# Login and Auth
## What is Role-Based Access Control (RBAC)?
Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.

----
## EXAMPLES OF ROLE-BASED ACCESS CONTROL

### Some of the designations in an RBAC tool can include:

  * Management role scope – it limits what objects the role group is allowed to manage.
  * Management role group – you can add and remove members.
  * Management role – these are the types of tasks that can be performed by a specific role group.
  * Management role assignment – this links a role to a role group.

 By adding a user to a role group, the user has access to all the roles in that group. If they are removed, access becomes restricted. Users may also be assigned to multiple groups in the event they need temporary access to certain data or programs and then removed once the project is complete.

Other options for user access may include:

 * Primary – the primary contact for a specific account or role.
 * Billing – access for one end-user to the billing account.
 * Technical – assigned to users that perform technical tasks.
 * Administrative – access for users that perform administrative tasks.

 ---
 ## BENEFITS OF RBAC

Managing and auditing network access is essential to information security. Access can and should be granted on a need-to-know basis. With hundreds or thousands of employees, security is more easily maintained by limiting unnecessary access to sensitive information based on each user’s established role within the organization.
### Other advantages include:

 1. Reducing administrative work and IT support. 
 2. Maximizing operational efficiency.
 3. Improving compliance.

----
## BEST PRACTICES FOR IMPLEMENTING RBAC
 * Current Status
 * Current Roles
 * Write a Policy
 * Make Changes
 * Continually Adapt

 -----

 ## react-cookie

### Integrations
 * universal-cookie - Universal cookies for JavaScript
 * universal-cookie-express - Hook cookies get/set on Express for server-rendering

## Minimum requirement
### react-cookie @ v3.0+
 * React.js >= 16.3.0 (new context API + forward ref)
### react-cookie @ v0.0-v2.2
 * React.js >= 15
### Getting started
 * npm install react-cookie

or in the browser (global variable ReactCookie):

```
<script
  crossorigin
  src="https://unpkg.com/react@16/umd/react.production.js"
></script>
<script
  crossorigin
  src="https://unpkg.com/universal-cookie@3/umd/universalCookie.min.js"
></script>
<script
  crossorigin
  src="https://unpkg.com/react-cookie@3/umd/reactCookie.min.js"
></script>
```
```
<CookiesProvider />
```

Set the user cookies

On the server, the cookies props must be set using req.universalCookies or new Cookie(cookieHeader)

* useCookies([dependencies])
Access and modify cookies using React hooks.

```
const [cookies, setCookie, removeCookie] = useCookies(['cookie-name']);
```

React hooks are available starting from React 16.8

dependencies (optional)
Let you optionally specify a list of cookie names your component depend on or that should trigger a re-render. If unspecified, it will render on every cookie change.

cookies
Javascript object with all your cookies. The key is the cookie name.

setCookie(name, value, [options])
Set a cookie value

 * name (string): cookie name
 * value (string|object): save the value and stringify the object if needed
 * options (object): Support all the cookie options from RFC 6265
    * path (string): cookie path, use / as the path if you want your cookie to be accessible on all pages
    * expires (Date): absolute expiration date for the cookie
    * maxAge (number): relative max age of the cookie from when the client receives it in seconds
    * domain (string): domain for the cookie (sub.domain.com or .allsubdomains.com)
    * secure (boolean): Is only accessible through HTTPS?
    * httpOnly (boolean): Can only the server access the cookie? Note: You cannot get or set httpOnly cookies from the browser, only the server.
    * sameSite (boolean|none|lax|strict): Strict or Lax enforcement

### removeCookie(name, [options])
Remove a cookie

 * name (string): cookie name
 * options (object): Support all the cookie options from RFC 6265
    * path (string): cookie path, use / as the path if you want your cookie to be accessible on all pages
    * expires (Date): absolute expiration date for the cookie
    * maxAge (number): relative max age of the cookie from when the client receives it in seconds
    * domain (string): domain for the cookie (sub.domain.com or .allsubdomains.com)
    * secure (boolean): Is only accessible through HTTPS?
    * httpOnly (boolean): Can only the server access the cookie? Note: You cannot get or set httpOnly cookies from the browser, only the server.
    * sameSite (boolean|none|lax|strict): Strict or Lax enforcement

## withCookies(Component)
----

Give access to your cookies anywhere. Add the following props to your component:

 * cookies: Cookies instance allowing you to get, set and remove cookies.
* allCookies: All your current cookies in an object.
Your original static properties will be hoisted on the returned component. You can also access the original component by using the WrappedComponent static property. Example:

```
function MyComponent() {
  return null;
}
const NewComponent = withCookies(MyComponent);
NewComponent.WrappedComponent === MyComponent;
```
## Cookies
~~~
get(name, [options])
~~~
Get a cookie value

 * name (string): cookie name
 * options (object):
    * doNotParse (boolean): do not convert the cookie into an object no matter what
```
 getAll([options])
```
### Get all cookies

 * options (object):
    * doNotParse (boolean): do not convert the cookie into an object no matter what
~~~
set(name, value, [options])
~~~
### Set a cookie value

 * name (string): cookie name
 * value (string|object): save the value and stringify the object if needed
 * options (object): Support all the cookie options from RFC 6265
    * path (string): cookie path, use / as the path if you want your cookie to be accessible on all pages
    * expires (Date): absolute expiration date for the cookie
    * maxAge (number): relative max age of the cookie from when the client receives it in seconds
    * domain (string): domain for the cookie (sub.domain.com or .allsubdomains.com)
    * secure (boolean): Is only accessible through HTTPS?
    * httpOnly (boolean): Can only the server access the cookie? Note: You cannot get or set httpOnly cookies from the browser, only the server.
    * sameSite (boolean|none|lax|strict): Strict or Lax enforcement

---
## remove(name, [options])
### Remove a cookie

 * name (string): cookie name
 * options (object): Support all the cookie options from RFC 6265
    * path (string): cookie path, use / as the path if you want your cookie to be accessible on all pages
    * expires (Date): absolute expiration date for the cookie
    * maxAge (number): relative max age of the cookie from when the client receives it in seconds
    * domain (string): domain for the cookie (sub.domain.com or .allsubdomains.com)
    * secure (boolean): Is only accessible through HTTPS?
    * httpOnly (boolean): Can only the server access the cookie? Note: You cannot get or set httpOnly cookies from the browser, only the server.
    * sameSite (boolean|none|lax|strict): Strict or Lax enforcement


