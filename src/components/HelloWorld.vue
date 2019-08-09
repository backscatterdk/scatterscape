<template>
  <div class="hello">
    <h1>{{ multiplied }}</h1>
   </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  computed: {
    multiplied: function () {return this.msg * this.msg}
  }
}
</script>
