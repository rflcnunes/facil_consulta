<template>
  <b-row id="progress-component">
<!--    <b-col cols="6" md="8">-->
<!--      <b-progress-->
<!--          :value="value * (1 / 2)"-->
<!--          :max="max"-->
<!--          class="mb-3 pull-left progress-component"></b-progress>-->
<!--    </b-col>-->
<!--    <b-col cols="1" md="4">-->
<!--      <div @click="randomValue" class="pull-right">{{ step }} de {{ steps }}</div>-->
<!--    </b-col>-->
    <div class="progress">
      <div class="progress-bar" id="progress-bar" role="progressbar" :aria-valuenow="value" :aria-valuemin="min" :aria-valuemax="max"></div>
    </div>
    {{ step }} de {{ steps }}
  </b-row>
</template>

<script>
export default {
  name: "ProgressComponent",
  data() {
    return {
      value: 1,
      min: 0,
      max: 4,
      item: '',
      step: 1,
      steps: 2,
    }
  },
  methods: {
    randomValue() {
      this.value = Math.random() * this.max
    },
  }
}
</script>

<style lang="scss" scoped>
#progress-component {
  display: flex;
  align-items: center;
  margin: 10px 0 10px 0;
  justify-content: space-between;
}

.progress {
  max-width: 80%;
  min-width: 80%;
  font-family: 'Open Sans', sans-serif;
}

#progress-bar {
  width: 100%;
  background-color: #483698;
}

</style>