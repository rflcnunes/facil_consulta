<template>
  <div id="subtitle-text-component">
    <h5 id="secondary-text">{{ title }}</h5>
  </div>
</template>

<script>
export default {
  name: "SubtitleTextComponent",
  props: ['title']
}
</script>

<style scoped>
#subtitle-text-component {
  margin-bottom: 25px;
}
</style>