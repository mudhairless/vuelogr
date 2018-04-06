# vuelogr

Simple but functional logging for Vue Components.

## Install

  `npm install --save vuelogr`

  `yarn add vuelogr`

## Usage

### Setup

Initialize the plugin where you initialize any other plugins in use with Vue. My recommended method is:

  `Vue.use(require('vuelogr'));`

This plugin uses your NODE_ENV and will only log when it is not equal to production.

### Components

To get full use of the plugin you must give you components a name property. I recommend placing this property at the top of the component.

```javascript
  export default {
    name: 'MyComponent'
    ...
  }
```

And to use simply call the $log method on the instance.

```javascript
  this.$log('This is important info I want to know.');
```
