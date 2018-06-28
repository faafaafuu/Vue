<template>
    <div id="app">
        <h1>{{msg}}</h1>
        <p>Hello Vuerld</p>
        {{msg}}
    </div>
</template>
<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>