<template>
<div id="select-states-component">
  <label id="label" for="select">{{ title }}</label>
  <select id="select" :title="posts">
    <option selected id="ghost-option">Selecione</option>
    <option v-for="state in states" :key="state.nome">{{ state.nome }}</option>
  </select>
</div>
</template>

<script>
import axios from 'axios'

export default {
  name: "SelectStatesComponent",
  props: ['title', 'posts'],
  data() {
    return {
      states: [],
    }
  },
  created() {
    this.getAllCities();
  },
  methods: {
    getAllCities() {
      axios.get('https://api-teste-front-end-fc.herokuapp.com/estados')
          .then((response) => {
        this.states = response.data;
      })
    }
  }
}
</script>

<style scoped>
#select-states-component {
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

#select {
  border: 1px solid #483698;
  border-radius: 5px;
  font-size: smaller;
  padding: 3px 0 3px 13px;
}

#ghost-option {
  color: gray;
}

</style>