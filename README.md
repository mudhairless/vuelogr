# vuelogr

Simple but functional logging for Vue Components.

## Install

  `npm install --save vuelogr`

  `yarn add vuelogr`

## Usage

### Setup

Initialize the plugin where you initialize any other plugins in use with Vue. My recommended method is:

  ```javascript
  Vue.config.debug = true; // remove to disable logging
  Vue.use(require('vuelogr'));
  ```

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

  this.$log('This message provides context for the second parameter', mydata);
```

You can enable logging without turning Vue's debug mode on with the $logStatus instance method.
This also allows you to enable or disable logging for specific components. This function does not
work at the global level.

```javascript
  this.$logStatus(true); //Enable logging for this component
  this.$logStatus(false); //Disable logging for this component
  const logEnabled = this.$logStatus(); //Get the status of logging for this component
```
