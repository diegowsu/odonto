<template>
  <div class="signup">
    <h2>Create New Account</h2>
    <form method="post" action="/auth/signup" name="signup">
      <div class="form-group">
        <div class="input-group">
          <input type="text" id="email" required="required"/>
          <label class="control-label" for="email">E-mail</label><i class="bar"></i>
        </div>
      </div>
      <div class="form-group">
        <div class="input-group">
          <input type="password" id="password" required="required"/>
          <label class="control-label" for="password">Senha</label><i class="bar"></i>
        </div>
      </div>
      <div class="abc-checkbox abc-checkbox-primary">
        <input id="checkbox1" type="checkbox" checked>
        <label for="checkbox1">
          <span class="abc-label-text">Eu concordo com <router-link to="">Termos de Uso.</router-link></span>
        </label>
      </div>
      <div class="d-flex flex-column flex-lg-row align-items-center justify-content-between down-container">
        <button class="btn btn-primary" type="submit">
          Sign Up
        </button>
        <router-link class='link' :to="{name: 'Login'}">Já cadastrado?</router-link>
      </div>
    </form>
  </div>
</template>

<script>
  export default {
    name: 'signup'
  }
</script>

<style lang="scss">
  @import '../../../sass/variables';
  @import '../../../../node_modules/bootstrap/scss/mixins/breakpoints';
  @import '../../../../node_modules/bootstrap/scss/variables';

  .signup {
    @include media-breakpoint-down(md) {
      width: 100%;
      padding-right: 2rem;
      padding-left: 2rem;
      .down-container {
        .link {
          margin-top: 2rem;
        }
      }
    }

    h2 {
      text-align: center;
    }
    width: 21.375rem;

    .down-container {
      margin-top: 2.6875rem;
    }
  }
</style>
