<template>
  <v-app>
    <v-toolbar dark>
      <v-toolbar-title class="white--text">
        <div class="toolbar-logo">
          <div class="toolbar-logo__circle"></div>
          <div class="toolbar-logo__text">EConnect</div>
        </div>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <div class="toolbar-actions">
          <v-btn class="btn_already-user" flat>Already a user?</v-btn>
          <v-btn class="btn_login" flat>Login</v-btn>
        </div>
      </v-toolbar-items>
    </v-toolbar>
    <v-content>
      <v-container fluid>
        <v-slide-y-transition mode="out-in">
          <Login/>
        </v-slide-y-transition>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import Login from './components/Login'

export default {
  name: 'App',
  components: {
    Login
  }
}
</script>

<style lang="scss">
  .v-toolbar {
    background-color: #6786a5 !important;
  }

  .toolbar-logo, .toolbar-actions {
    margin-left: 44px;
    display: flex;
    justify-content: flex-start;
    &__circle {
      width: 20px;
      height: 20px;
      border-radius: 50%;
      background: #ffffff;
    }
    &__text {
      margin-left: 12px;
      color: #ffffff;
      font-family: Roboto;
      font-size: 16px;
    }
  }

  .btn_already-user {
    width: 10px;
    font-size: 16px;
  }

  .btn_login {
    width: 46px;
    margin-left: 8px;
    font-size: 18px;
  }
</style>
