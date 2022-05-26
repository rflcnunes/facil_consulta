<template>
<div id="header-text-component">
  <h2 id="principal-text">{{ title }}</h2>
</div>
</template>

<script>
export default {
  name: "HeaderTextComponent",
  props: ['title']
}
</script>

<style scoped>
#principal-text {
  font-family: 'Comfortaa', cursive;
  margin-top: 10px;
  margin-bottom: 25px;
  color: #483698;
}

</style>