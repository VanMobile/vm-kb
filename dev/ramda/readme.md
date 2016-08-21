## ramda repl:
http://ramdajs.com/repl

```js
// es6 js function expression syntax: 
const f = () => { };

// shortform syntax
const add = (a, b) => a + b;

// longform syntax
const add = (a, b) => {
 return a + b; 
};
```
For more details see...  
http://goo.gl/VzDmpH



```js
## ramda curry:
const ad = (a, b) => a + b;
const adc = R.curry(ad);

const ad4 = adc(4);
ad4(5);
//=> 9


```
For more details see...  
http://goo.gl/SJgzan
