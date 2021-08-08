# RestfulAPITest

### Vue project Create All Default selected
```
vue create restfultest  
cd restfultest
vue add vuetify
vue add router
```
Create .eslintignore files
```
/build/**
/coverage/**
/docs/**
/jsdoc/**
/templates/**
/tests/bench/**
/tests/fixtures/**
/tests/performance/**
/tmp/**
/tools/internal-rules/node_modules/**
/lib/rules/utils/unicode/is-combining-character.js
test.js
!.eslintrc.js
/src/**
```
add Axios
```
vue add axios
```
### Create Environment variable
Create .env  
```
I'll Send this files by email 
```
Create .env.local  
```
I'll Send this files by email 
```
Create .env.production
```
I'll Send this files by email 
```
add Authentication Module
```
npm install vue-msal
```
edit @/src/main.js
```
import Vue from 'vue'
import './plugins/axios'
import App from './App.vue'
import vuetify from './plugins/vuetify';
import router from './router'
import msal from 'vue-msal' // For Authentication Module

Vue.config.productionTip = false 

// For Authentication Module
Vue.use(msal, {
  auth: {
    clientId: process.env.VUE_APP_CLIENT_ID,
    tenantId: process.env.VUE_APP_TENANT,
    redirectUri: process.env.VUE_APP_REDIRECT,
    scopes: process.env.VUE_APP_XSCOPE
  }
});
new Vue({
  vuetify,
  router,
  render: h => h(App)
}).$mount('#app')
```
