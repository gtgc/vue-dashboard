<template>
  <nav
    id="nav"
    class="navbar is-spaced"
    role="navigation"
    aria-label="main navigation"
    style="border-bottom: 2px solid #f5f5f5"
  >
    <div id="navbar" class="navbar-menu">
      <div class="navbar-start">
        <a class="navbar-item">
          <router-link to="/"> <Home /> </router-link>
        </a>

        <a class="navbar-item"
          ><router-link to="/documentation">Documentation</router-link>
        </a>
      </div>

      <div class="navbar-end">
        <User />
      </div>
    </div>
  </nav>
</template>

<script>
import Home from "@/components/Home.vue";
import User from "@/components/User.vue";
export default {
  components: {
    Home,
    User,
  },
};
</script>

<style lang="sass">
.icon svg
    color: #42b983
</style>