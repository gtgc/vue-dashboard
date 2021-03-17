<template>
  <div class="navbar-item has-dropdown is-hoverable">
    <a class="navbar-link is-arrowless" @click="userClicked">
      <span v-if="userName" style="padding-right: 10px"
        >Welcome {{ userName }}!</span
      >
      <span class="icon">
        <span class="icon-text">
          <span class="icon">
            <fa icon="user" class="iconColor" type="fas"></fa>
          </span>
        </span>
      </span>
    </a>

    <div class="navbar-dropdown is-right" id="content1" v-if="userName === ''">
      <a class="navbar-item" @click="mockLogin"> Login </a>
      <a class="navbar-item"> Register </a>
    </div>
    <div class="navbar-dropdown" id="content2" v-else>
      <a class="navbar-item"> Profile </a>
      <a class="navbar-item"> Account </a>
      <hr class="navbar-divider" />
      <a class="navbar-item" @click="mockLogout"> Logout </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: false,
      userName: "",
      userButton: {
        isMedium: false,
      },
    };
  },
  methods: {
    userClicked() {
      this.isActive = !this.isActive;
    },
    mockLogin() {
      this.userName = "Tugce";
      this.isActive = !this.isActive;
      this.userButton.isMedium = !this.userButton.isMedium;
    },
    mockLogout() {
      this.userName = "";
      this.isActive = !this.isActive;
      this.userButton.isMedium = !this.userButton.isMedium;
    },
  },
};
</script>

<style lang="sass" scoped>
.icon fa
    color: #42b983
</style>