<template>
  <header class="top-header">
    <div class="util__flex util__container top-header-container">
      <nav class="top-header__col">
        <ul class="top-header__nav">
          <li v-for="(navitem, index) in $store.state.settings.main_navi" :key="index">
            <nuxt-link class="top-header__link" :to="navitem.Link.cached_url">
              {{ navitem.Text }}
            </nuxt-link>
          </li>
        </ul>
      </nav>
      <a href="/" class="top-header__col top-header__logo">
        Deputy
      </a>
      <nav class="top-header__col top-header__second-navi">
        <ul class="top-header__nav top-header__nav--right">
          <li>
            <nuxt-link class="top-header__link" to="/en/blog">
              English
            </nuxt-link>
          </li>
          <li>
            <nuxt-link class="top-header__link" to="/de/blog">
              German
            </nuxt-link>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss">
@import '../assets/scss/variables.scss';

.top-header {
  background-color:  $blue-dark;
}

.top-header-container {
  justify-content: space-between;
  padding-top: 30px;
  padding-bottom: 30px;
}

.top-header__logo {
  text-align: center;

  svg {
    max-height: 30px;
  }
}

.top-header__second-navi {
  text-align: right;
}

.top-header__nav {
  list-style-type: none;

  a {
    color: $white;

    &:hover {
      color: $grey-light;
    }
  }
}
</style>
