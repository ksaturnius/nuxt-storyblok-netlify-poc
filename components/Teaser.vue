<template>
  <div v-editable="blok">
    {{ blok.headline }}
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line
  props: ['blok']
}
</script>
