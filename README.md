# vjs-cookie (Vanilla Javascript Cookies)
Lightweight JavaScript for handling cookies.\
size: 1.44kb

## CDN jsdelivr
```html
<script src="https://cdn.jsdelivr.net/gh/Hillzacky/vjs-cookie/vjs.cookie.js"></script>
```
## Basic Usage

Create cookie:

```javascript
Cookies.set('key', 'value')
Cookies.set('key', 'value', { expires: 7 }) /* Expires 7 days */
Cookies.set('key', 'value', { expires: 7, path: '' }) /* Create an expiring cookie */
```

Read cookie:

```javascript
Cookies.get('key') /* Showing: 'value' */
Cookies.get('nothing') /* Showing: undefined */
Cookies.get() /* Read all Cookies */
```

Delete cookie:

```javascript
Cookies.remove('key')
Cookies.remove('key', { path: '' }) /* Delete a cookie valid to the path of the current page */
Cookies.remove('key', { path: '', domain: '.domain.com' })
```

### domain

```javascript
Cookies.set('key', 'value', { domain: 'subdomain.domain.com' })
Cookies.get('key') /* Showing: undefined (need to read at 'subdomain.domain.com') */
```

### secure (boolean)

```javascript
Cookies.set('key', 'value', { secure: true }) /* Default: false */
Cookies.get('key') /* Showing: 'value' */
Cookies.remove('key')
```

### Same Site

```javascript
Cookies.set('key', 'value', { sameSite: 'strict' }) /* Default: not set */
Cookies.get('key') /* Showing: 'value' */
Cookies.remove('key')
```
