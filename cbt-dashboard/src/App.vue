<template>
  <div id="app">
    <!--<UserPage />-->
    <UserInfo />
  </div>
</template>

<script>
//import UserPage from './components/UserPage.vue';
import UserInfo from './components/UserInfo.vue';

export default {
  name: 'App',
  components: { UserInfo },
  //components: { UserPage }
}
</script>

<style>
</style>
