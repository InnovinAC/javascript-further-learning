An interesting discovery. Tagged Template Literals

The function that precedes the template literal is called a tag function. When the tag function gets called, the first argument it receives is an array of strings. This array is the result of splitting the template literal on the interpolated parts.
The rest of the arguments would be an array of the variables in the string literal.

```js
const logSomething = (name, ...rest) => {
console.log(name)
}
const name = 'Innovin'

logSomething`hello ${name}. Welcome`   
```
Output is `["hello ", ". Welcome"]`


Also:

```js
const logSomething = (name, ...rest) => {
console.log(rest)
}
const name = 'Innovin'

logSomething`hello ${name}. Welcome`   
```
Output is `["Innovin"]`

