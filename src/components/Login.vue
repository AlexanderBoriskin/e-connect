<template>
  <v-layout class="login-page" column align-center>
    <div class="login-page__above-body">
      <div class="e-connect-circle"></div>
      <div class="e-connect-text">
        EConnect
      </div>
    </div>
    <v-card class="login-page__card">
      <div class="login-page__body">
        <v-btn class="linkedin-btn primary-btn">
          <span class="linkedin-btn__text">
            Log In With LinkedIn
          </span>
          <img class="linkedin-btn__icon" src="../../src/assets/linked-in.png"/>
        </v-btn>
        <div class="text_or text-lg-center">
          OR
        </div>
        <v-text-field v-model="email" label="Email" required/>
        <v-text-field v-model="password" label="Password" required/>
        <v-btn class="login-btn secondary-btn">
          Log In With Email
        </v-btn>
        <div class="text_forgot-password text-lg-center">
          Forgot password?
        </div>
      </div>
    </v-card>
    <div class="login-page__below-body">
      <div class="question-text">
        Don't have an account?
      </div>
      <v-btn class="secondary-btn">Sign Up</v-btn>
    </div>
  </v-layout>
</template>

<script>
export default {
  name: 'Login',
  data: function () {
    return {
      email: '',
      password: ''
    }
  }
}
</script>

<style lang="scss">
  .login-page {

    &__above-body {
      height: 40px;
      margin-top: 44px;
      margin-bottom: 56px;
      display: flex;
      justify-content: flex-start;
      .e-connect-circle {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background: #b4d4fa;
      }

      .e-connect-text {
        margin-left: 20px;
        color: #9b9b9b;
        font-family: Roboto;
        font-size: 32px;
      }
    }

    &__card {
      border: 0 !important;
      border-radius: 20px;
    }

    &__body {
      width: 471px;
      padding: 40px 100px;

      .linkedin-btn {
        &__text {
          width: 146px;
          text-align: left;
        }

        &__icon {
          margin-left: 33.5px;
        }

        .v-btn__content {
          justify-content: flex-start !important;
          padding-left: 24.5px;
        }
      }

      .login-btn {
        margin-top: 17px !important;
      }

      .v-text-field {
        margin-top: 0;
        padding-top: 0;
        .v-input__slot {
          margin-bottom: 4px;
          &:before {
            border-style: none !important;
          }
        }
        &__slot {
          border: 2px solid #ececec;
          .v-label {
            margin-left: 15.4px;
            color: #9b9b9b;
            font-family: Gotham;
            font-size: 14px;
          }
        }
      }

      .text_or {
        padding: 47px 0;
      }
      .text_forgot-password {
        margin-top: 31px;
      }
    }

    &__below-body {
      .question-text {
        height: 29px;
        margin-top: 54px;
        margin-bottom: 42px;
        font-family: Gotham;
        font-size: 24px;
        color: #4a4a4a;
      }
    }

  }

  .v-btn {
    width: 100%;
    margin: 0 !important;
    .v-btn__content {
      text-transform: none !important;
      color: white !important;
    }
  }

  .secondary-btn {
    background-color: #46a29f !important;
  }

  .primary-btn {
    background-color: #147dbe !important;
  }

  .container {
    background: #f6f7f7;
  }
</style>
