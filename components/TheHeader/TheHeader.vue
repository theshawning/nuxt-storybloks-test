<template>
  <header class="main-header">
    <nav class="main-nav">
      <ul class="nav-links">
        <nuxt-link to="/" tag="li" class="nav-link">
          <a>All Posts</a>
        </nuxt-link>
        <nuxt-link to="/about" tag="li" class="nav-link">
          <a>About</a>
        </nuxt-link>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.main {
  &-header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background: #022d30;
    height: 4.5rem;
  }

  &-nav {
    height: 100%;
  }
}

.nav-links {
  list-style: none;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}

.nav-link {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 1rem;
  padding: 0.3rem;

  &.nuxt-link-exact-active {
    border-bottom: 3px solid #06c4d1;
  }

  & a {
    display: block;
    text-decoration: none;
    color: white;

    &:hover,
    &:active {
      color: #06c4d1;
    }
  }
}

.nuxt-link-exact-active a {
  color: #06c4d1;
}
</style>