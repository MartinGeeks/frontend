<template>
  <f7-page login-screen>
    <f7-block
      class="login-content"
    >
      <f7-row class="content-login">
        <f7-col width="100">
          <div>
            <img
              :src="logoLogin"
              width="85%"
              class="margin-left"
            >
          </div>
        </f7-col>
        <f7-col width="100">
          <f7-list
            id="list-form"
            form
          >
            <f7-list-input
              outline
              label="Usuario"
              item-label
              type="text"
              placeholder="Usuario"
              clear-button
              name="username"
              max="255"
              autocomplete="on"
              required
              @input="username = $event.target.value"
            />
            <!-- Password -->
            <f7-list-input
              outline
              label="Contraseña"
              item-label
              type="password"
              placeholder="Contraseña"
              clear-button
              name="password"
              max="255"
              autocomplete="current-password"
              required
              @input="password = $event.target.value"
            />
          </f7-list>
        </f7-col>
        <f7-col width="100">
          <f7-list>
            <f7-button
              col
              button
              button-large
              button-raised
              fill
              href="/main/"
            >
              Entrar
            </f7-button>
            <f7-button
              col
              button
              button-large
              button-raised
              outline
              href="/register/"
              class="margin-top"
            >
              Registrarse
            </f7-button>
          </f7-list>
        </f7-col>
      </f7-row>
    </f7-block>
  </f7-page>
</template>

<script>

import logoLogin from '../static/img/appastradarklogin.png';

export default {
  name: 'Login',
  data() {
    return {
      username: '',
      password: '',
    };
  },
  computed: {
    logoLogin() {
      return logoLogin;
    },
  },

  methods: {

  },
};
</script>

<style scoped>
  .login-content{
    padding-left: 4em;
    padding-right: 4em;
    padding-top: 6em;
    padding-bottom: 6em;
    border: 2px solid rgb(31, 31, 31);
    transition: 0.6s all;
  }

  .login-content:hover {
    box-shadow: 10px 10px 14px 1px rgba(145,126,145,1);
  }
</style>
