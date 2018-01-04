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

* "exist" will "plus" or "use"

Base:

```javascript
if (exist) {
  plus++;
}
```

Enchating:

```javascript
exist && plus++;

// or

window.exist && exist.doSomething;
```



### Base object

**In fact, you do not need to consider all, because you can know how many types will appear.**

* Basic Type
  * Null

    ```javascript
    if(obj)
    ```

  * Undefine

    ```javascript
    if(x)
    ```

  > Remember, `Null` represents this shouldn't have value，but `undefine` is not. 
  >
  > So `Number(null) === 0` , but `Number(undefined)` is `NaN`

  > Importantly, if(0) is very dangerous!

  * Number

    * isNumber

      ```javascript
      typeof number === 'number' && isFinite(number); // isFinite avoids NaN
      ```
      > Do not use `isNaN` , cause non-numbers will coerced to numeric type.

    * Integer

      ```javascript
      Number.isInteger(); // ES6, SO GOOD!
      ```

  * Boolean

    ```javascript
    typeof val === 'boolean';
    ```

  * String

    ```javascript
    typeof str === 'string'; // && str.length > 0 
    ```

  * Symbol (ES6)

    ```javascript
    typeof s === 'symbol'; 
    ```

* Reference Type （ Just in common use）
  * Object

    ```javascript
    typeof obj === 'object' && obj instanceof Object
    ```

  * Array

    ```javascript
    typeof arr === 'array' && arr instanceof Array
    ```

  * Function

    ```javascript
    typeof fun === 'function' && arr instanceof Function
    ```

* Other

  * JSON-String

    ```javascript
    function isJSON(str) {
            if (typeof str == 'string') {
                try {
                    var obj=JSON.parse(str);
                    if(str.indexOf('{')>-1){
                        return true;
                    }else{
                        return false;
                    }

                } catch(e) {
                    console.log(e);
                    return false;
                }
            }
            return false;
    }
    ```

    ​



## Function

### Concept

* Use arrow function



## algorithm







## Hack

