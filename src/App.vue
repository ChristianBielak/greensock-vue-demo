<template>
  <div id="app">
    <nav class="navbar is-fixed-top">
      <div class="navbar-brand">
        <a class="navbar-item" href="#">
          Frogbob
        </a>
        <div class="navbar-burger burger" :class="{'is-active' : isActive}" @click="isActive = !isActive">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>

      <div id="navbarExampleTransparentExample" class="navbar-menu" :class="{'is-active' : isActive}">
        <div class="navbar-start">
          <router-link to="/" class="navbar-item">
            Home
          </router-link>
        </div>
      </div>
    </nav>

    <router-view class="content"></router-view>
  </div>
</template>

<script>
export default {
  name: 'App',
    data(){
      return{
          isActive: false
      }
    }
};
</script>

<style>
.content{
  margin-top: 52px;
}
</style>
