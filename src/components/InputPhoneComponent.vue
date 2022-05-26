<template>
  <div id="input-component">
    <label id="label" for="input">{{ title }}</label>
    <the-mask id="input" :mask="['(##) ####-####', '(##) #####-####']" :placeholder="placeholder"/>
  </div>
</template>

<script>

export default {
  name: "InputPhoneComponent",
  props: ['title', 'placeholder'],
}
</script>

<style scoped>
#input-component {
  display: flex;
  flex-direction: column;
  max-width: 65%;
  min-width: 65%;
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