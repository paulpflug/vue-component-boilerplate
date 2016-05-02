// out: ..
<template lang="{{template}}">
{{#if_eq template "html"}}
<div class="component">hello
  <input v-model="greeting"></input>
</div>
{{/if_eq}}
{{#if_eq template "pug"}}
.component hello
  input(v-model="greeting")
{{/if_eq}}
</template>

<script {{#if_eq script "coffee"}}lang="{{script}}"{{/if_eq}}>
{{#if_eq script "es5"}}
module.exports = {
  data: function() {
    return { greeting: "World" }
  }
}
{{/if_eq}}
{{#if_eq script "es6"}}
export default {
  data: () => {
    return { greeting: "World" }
  }
}
{{/if_eq}}
{{#if_eq script "coffee"}}
module.exports =
  data: ->
    greeting: "World"
{{/if_eq}}
</script>

{{#ifstyle}}
<style lang="{{style}}">
.component {
  margin: 0 auto;
}
</style>
{{/ifstyle}}
