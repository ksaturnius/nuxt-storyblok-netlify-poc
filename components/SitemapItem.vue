<template>
  <li class="sitemap-item">
    <nuxt-link :to="'/' + model.item.slug">
      {{ model.item.name }}
    </nuxt-link>
    <ul v-if="model.children.length > 0">
      <sitemap-item
        v-for="item in model.children"
        :key="item.item.id"
        :model="item"
      />
    </ul>
  </li>
</template>

<script>
export default {
  // eslint-disable-next-line
  props: ['model']
}
</script>

<style lang="scss">
.sitemap-item {
  padding: 5px 0;

  a {
    color: #8ba19a;
  }

  ul {
    margin-top: 10px;
    margin-bottom: 10px;
  }
}
</style>
