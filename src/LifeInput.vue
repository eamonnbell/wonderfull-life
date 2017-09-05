<template>
    <input 
        type="text"
        v-bind:value="value"
        v-on:input="updateValue($event.target.value)"
        autofocus>
</template>
<script>
export default {
  name: 'life-input',
  props: ['value'],
  methods: {
      updateValue(value){
          this.$emit('input', value);
      }
  }
}
</script>
<style scoped>
    input[type="text"] {
        background: rgba(0, 0, 0, 0);
        border: 1px solid black;
        outline: none;
        text-shadow: 2px 2px 0px #999;
        font-size: 48px;
        padding: 10px;
    }
</style>
