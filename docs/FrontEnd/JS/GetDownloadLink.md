# Get Download Link

## JS

```js
console.log([...document.querySelectorAll('a[href$=".zip"]')].map(anchor => anchor.href).join('\n'));
```

## Example

https://dl.cv.ethz.ch/bdd100k/data/
