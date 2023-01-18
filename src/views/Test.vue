<script>
import Button from "@/components/icons/Button.vue";
export default {
  name: "Test",
  components: {
    Button,
  },
  data(){
    return{
      title: "Button1",

    }
  },
  methods: {
    sayHello(){
      alert("hi vue people")
    }
  }
}
</script>

<template>

  <Button :title="title" :whenClicked="sayHello"/>
</template>



<style scoped>

</style>