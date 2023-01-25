<template>
  <div id="app">
    <!--<UserInfo />-->
    <UserTable />
  </div>
</template>

<script>
//import UserInfo from './components/UserInfo.vue';
import UserTable from './components/UserTable.vue';

export default {
  name: 'App',
  //components: { UserInfo },  //components: { UserPage },
  components: { UserTable }
}
</script>

<style>
</style>
