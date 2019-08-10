# Reproduction for Babel+Svelte+(IE11/iOS9) issue

There seems to be some sort of interop issue with Babel/core-js and Svelte on older browsers.

Browsers currently known affected:

- IE 11
- iOS 9 Mobile Safari

Stack trace when app loaded (originating from core-js)

```
[Error] TypeError: Type error
	toString (bundle.js:312:95)
	toString (bundle.js:312:95)
	_isNativeFunction (bundle.js:11152)
	_wrapNativeSuper (bundle.js:11290)
	_wrapNativeSuper (bundle.js:11317)
	(anonymous function) (bundle.js:12708)
	Global Code (bundle.js:12814)
```

## How to run

Install the dependencies...

```bash
cd cloned
npm install
```

...then start (not in dev mode, because live reload breaks in old browsers)

```bash
npm run build
npm run start
```

...then launch either Mobile Safari on iOS 9 (XCode Simulator!) or IE 11 in Windows.

Navigate to [localhost:5000](http://localhost:5000) and open the console.

# 💥
