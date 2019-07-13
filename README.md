# Awesome Web Components Snippets

## Async interface for enqueuing callbacks that run at microtask timing

```js
// Polymer lib
// https://polymer-library.polymer-project.org/3.0/api/utils/async#microTask.run
// https://github.com/Polymer/polymer/blob/master/lib/utils/async.js#L174
microTask.run(callback);
Polymer.async.microtask.run(callback);
// Vanilla code
Promise.resolve().then();
await 0
await new Promise(res => setTimeout(res));
```
[source](https://polymer.slack.com/archives/C03PF4L4L/p1562932408050200)

## Get a list of defined components

```js
const origDefine = window.customElements.define;
window.customElements.define = (name, clas) => {
  console.log(name);
  origDefine(name, clas);
}
```
[source](https://polymer.slack.com/archives/C03PF4L4L/p1562835614000100)
