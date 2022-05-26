<template>
  <div id="select-cities-component">
    <label id="label" for="select">{{ title }}</label>
    <select id="select" :title="posts">
      <option selected id="ghost-option">Selecione</option>
      <option v-for="city in cities" :key="city.nome">{{ city.nome }}</option>
    </select>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: "SelectCitiesComponent",
  props: ['title', 'posts'],
  data() {
    return {
      cities: [],
    }
  },
  created() {
    this.getAllCities();
  },
  methods: {
    getAllCities() {
      axios.get('https://api-teste-front-end-fc.herokuapp.com/cidades')
          .then((response) => {
            this.cities = response.data;
          })
    }
  }
}
</script>

<style scoped>
#select-cities-component {
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