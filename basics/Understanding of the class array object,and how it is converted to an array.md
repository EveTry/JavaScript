# Understanding of the class array object,and how it is converted to an array
An object with the length attribute and several Index attributes can be called a class array object. Class array objects are similar to arrays, but array methods cannot be called. Common class array objects include arguments and DOM methods. Function parameters can also be considered as class array objects because they contain the length attribute value, which represents the number of parameters that can be received. 

There are several common methods to convert class arrays into arrays: 
- call the slice method of the array to implement conversion.
```js
Array.prototype.slice.call(arrayLike);
```
- call the splice method of an array to implement conversion.
```js
Array.prototype.splice.call(arrayLike, 0);
```
- use apply to call the concat method of an array to implement conversion
```js
Array.prototype.concat.apply([], arrayLike);
```
- use the Array.from Method to implement conversion
```js
Array.from(arrayLike);
```
