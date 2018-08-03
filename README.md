# enchating-js


## Common

### Concept
* Please code `===` instead of  `==`
* `;` make the world better,ignore [standardjs](https://standardjs.com/)
* Fxxx  `var` , strongly recommend `const` && `let`


### Less is more


* is -1 ?

Base:

```javascript
number === -1;
```

Enchating:
```javascript
!~number;
```

* rounding

Base:

```javascript
Math.round(1.2);
```

Enchating:

```javascript
~~1.2;
```

* default

Base:

```javascript
object ? object : {};
```

Enchating:

```javascript
let array = object || {};

// or

(arg1 = 1, arg2 = 2) => console.log(arg1, arg2);
```

* too many judgements ?

Base:

```javascript
let number = 5;
number === 5 ? doSomething() : false;
```

Enchating:

```javascript
let number = 5;
number === 5 || doSomething();
```

* "true", "false" ?

Base：

```javascript
let str = 'true';
return str === 'true';
```

Enchating:

```Javascript
let str = 'true';
return (/^true$/i).test(str); // set to util.js
```

* &&

Base:

```javascript
if (exist) {
  plus++;
}
```

Enchating:

```javascript
exist && plus++; // if exist, return plus++

// or

window.exist && exist.doSomething;
```

* ||

Base:

```javascript
if (!exist) {
  plus++;
}
```

Enchating:

```javascript
exist || plus++; //if not exist, return plus++

// or

window.exist || exist.doSomething;
```

- ++ or --

Base:

```javascript
if (a > 10) {
  doSomething()
}
a++; // a just a counter
```

Enchating:

```javascript
if (++a > 0) { // a just a counter
  doSomething()
}
```

### Tpye