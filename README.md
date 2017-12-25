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
number === 5 ? doSomething() : false
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

* "exist" will "plus" or "use"

Base:

```javascript
if (exist) {
  plus++;
}
```

Enchating:

```javascript
exist && plus++

// or

window.exist && exist.doSomething
```



### Base object

**In fact, you do not need to consider all, because you can know how many types will appear.**

* Basic Type
  * Null

    `if(obj)`

  * Undefine

    `if(x)`

  > Remember, `Null` represents this shouldn't have value，but `undefine` is not. 
  >
  > So `Number(null) === 0` , but `Number(undefined)` is `NaN`

  * Number
  * Boolean
  * String
  * Symbol
* Reference Type （ Just in common use ）
  * Object
  * Array
  * Function



## Function

### Concept

* Use arrow function



## algorithm







## Hack

