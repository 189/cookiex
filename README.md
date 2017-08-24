# Cookiex
HTTP cookie parser and serializer for javascript

## Usage

```
$ npm install cookiex --save
```
import and use it like below:

```
const cookiex = require('cookiex');
cookiex.set('name', 'obama', 3, 'baidu.com', '/', false);
cookie.get('name'); // return 'obama'
cookie.remove('name') // unset cookie
```

or if you import it as script link:  

```
<script src='./index.js'></script>
```	
`cookiex` will be expose in global scope.

```
cookiex.set('name', 'obama', 3, 'baidu.com', '/', false);
cookie.get('name'); // return 'obama'
cookie.remove('name') // unset cookie
```
## API
```
const cookiex = require('cookiex');
```

### cookiex.set(name)
* `name` the cookie name you want parse.  
	
### cookie.get(name, value, domain, expire, path, secure)

* `name` Cookie name.
* `value` Cookie value.
* `expire` Specifies the number (in days) to be the value for the Max-Age Set-Cookie attribute.
* `domain` Specifies the value for the Domain Set-Cookie attribute. By default, no domain is set, and most clients will consider the cookie to apply to only the current domain.
* `path` Specifies the value for the Path Set-Cookie attribute.
* `secure` Specifies the boolean value for the [Secure Set-Cookie attribute],when setting this to true, as compliant clients will not send the cookie back to the server in the future if the browser does not have an HTTPS connection.


### cookie.remove(name)