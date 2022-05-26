<template>
  <button type="button" id="button" @click="emit($event)">{{ title }}</button>
</template>

<script>
export default {
  name: "ButtonPrimary",
  props: ['title'],
    methods: {
      emit(event) {
        alert('hello')
        this.$emit('data', event)
      }
    }

}
</script>

<style scoped>
#button {
  min-width: 100%;
  max-width: 100%;
  border: 0;
  background-color: #483698;
  color: white;
  border-radius: 20px;
  font-family: 'Open Sans', sans-serif;
}

</style>