<template>
  <div class="app">
    <div class="social-nav">
      <SocialNav />
    </div>
    <h1 class="page-title">Ateljé by M</h1>
    <div class="nav">
      <router-link to="/">home</router-link> |
      <router-link to="/about">about</router-link> |
      <router-link to="/menu">menu</router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
import SocialNav from '@/components/SocialNav.vue';

export default {
  name: 'app',
  components: {
    SocialNav,
  }
}
</script>


<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Josefin+Sans&display=swap');

.app {
  font-family: 'Josefin Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
}

.nav {
  padding-bottom: 30px;
  a {
    font-weight: lighter;
    color: black;
    &.router-link-exact-active {
      color: #c7bbb8;
    }
    font-variant: small-caps;
    text-decoration: none;
    padding: 0px 10px;
  }
}

.social-nav {
  text-align: right;
}

.page-title{
  padding-top: 30px;
}

</style>
