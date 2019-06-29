<template>
  <div v-editable="blok" class="util__flex">
    <component :is="blok.component" v-for="blok in blok.columns" :key="blok._uid" :blok="blok" />
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line
  props: ['blok']
}
</script>
