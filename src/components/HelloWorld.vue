<template>
  <v-container fluid>
    <v-slide-y-transition mode="out-in">
      <v-layout column align-center>
        <div>
          EConnect
        </div>
        <v-card>
          <div style="padding: 20px 60px;">
            <div>
              <v-btn class="primary-btn">Log In With LinkedIn</v-btn>
            </div>
            <div class="text-lg-center">OR</div>
            <div>
              <v-text-field v-model="email" label="Email" required/>
            </div>
            <div>
              <v-text-field v-model="password" label="Password" required/>
            </div>
            <div>
              <v-btn class="secondary-btn">Log In With Email</v-btn>
            </div>
            <div class="text-lg-center">Forgot password?</div>
          </div>
        </v-card>
        <div class="question-text">
          Don't have an account?
        </div>
        <div>
          <v-btn class="secondary-btn">Sign Up</v-btn>
        </div>
      </v-layout>
    </v-slide-y-transition>
  </v-container>
</template>

<script>
export default {
  name: 'HelloWorld'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .v-card {
    border: 2px solid #ececec;
  }

  .v-text-field__slot {
    border: 2px solid #ececec;
  }

  .v-input__slot:before {
    border-style: none !important;
  }

  .question-text {
    font-family: Gotham;
    font-size: 24px;
    color: #4a4a4a;
  }

  .secondary-btn {
    background-color: #46a29f !important;
  }

  .primary-btn {
    background-color: #147dbe !important;
  }

  .v-btn__content {
    color: white !important;
  }

</style>
