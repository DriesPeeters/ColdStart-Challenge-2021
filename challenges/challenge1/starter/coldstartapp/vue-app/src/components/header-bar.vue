<script>
import HeaderBarBrand from '@/components/header-bar-brand.vue';
import AuthLogin from './auth-login.vue';
import AuthLogout from './auth-logout.vue';

export default {
  name: 'HeaderBar',
  components: {
    HeaderBarBrand,
    AuthLogin,
    AuthLogout,
  },
  data() {
    return {
    };
  },
  methods: {
  },
};
</script>

<template>
  <header>
    <nav class="navbar is-white" role="navigation" aria-label="main navigation">
      <HeaderBarBrand></HeaderBarBrand>
      <div class="navbar-menu">
        <div class="navbar-start">
          <router-link class="navbar-item nav-home" to="/">Home</router-link>
        </div>
        <div class="navbar-end">
          <div class="navbar-item auth-link">
            <AuthLogin provider="GitHub"/>
          </div>
          <div class="navbar-item auth-link">
            <AuthLogout/>
          </div>
        </div>
      </div>
      <AuthLogin></AuthLogin>
    </nav>
  </header>
</template>
