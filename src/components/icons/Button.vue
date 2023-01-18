<script>
export default {
  name: "Button",
  props: {
    title: String,
    whenClicked: Function,
    color: "red"
  }
}
</script>

<template>
  <button style="{backgroundColor: red}" @click="whenClicked">{{ title }}</button>
</template>



<style scoped>

</style>