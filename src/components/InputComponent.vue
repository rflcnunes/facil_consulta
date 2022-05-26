<template>
<div id="input-component">
  <label id="label" for="input">{{ title }}</label>
  <input id="input" type="text" :placeholder="placeholder">
</div>
</template>

<script>
export default {
  name: "InputComponent",
  props: ['title', 'placeholder']
}
</script>

<style scoped>
#input-component {
  display: flex;
  flex-direction: column;
  max-width: 100%;
  min-width: 100%;
  font-family: 'Open Sans', sans-serif;
  margin-top: 5%;
  margin-bottom: 5%;
}

#label {
  font-size: smaller;
  margin-bottom: 5px;
}

#input {
  border: 1px solid #483698;
  border-radius: 5px;
  font-size: smaller;
  padding: 3px 0 3px 13px;
}

input:focus {
  outline: none !important;
}

</style>