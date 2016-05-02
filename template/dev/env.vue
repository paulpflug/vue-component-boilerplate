<template lang="{{template}}">
{{#if_eq template "html"}}
<comp></comp>
{{/if_eq}}
{{#if_eq template "pug"}}
comp
{{/if_eq}}
</template>

<script {{#if_eq script "coffee"}}lang="{{script}}"{{/if_eq}}>
{{#if_eq script "es5"}}
module.exports = {
  components: {
    comp: require('../src/index.vue')
  }
}
{{/if_eq}}
{{#if_eq script "es6"}}
import { default as comp } from '../src/index.vue'
export default {
  components: {
    comp
  }
}
{{/if_eq}}
{{#if_eq script "coffee"}}
module.exports =
  components:
    "comp": require("../src/index.vue")
{{/if_eq}}
</script>

{{#ifstyle}}
<style lang="{{style}}">
</style>
{{/ifstyle}}
