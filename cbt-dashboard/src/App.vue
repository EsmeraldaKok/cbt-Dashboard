<template>
  <div id="app">
    <!--<UserInfo />
    <UserTable />
    <AddUser />
    <AddProject />-->
    <AddIndustry />
    
  </div>
</template>

<script>

//import UserInfo from './components/UserInfo.vue';
//import UserTable from './components/UserTable.vue';import AddUser from './components/AddUser.vue';
//import AddProject from './components/AddProject.vue';
//import AddUser from './components/AddUser.vue';
import AddIndustry from './components/AddIndustry.vue';
export default {
    name: "App",
    components: { AddIndustry }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;1,300;1,500;1,900&display=swap');
    
/* general  styles*/
*, 
*::after, 
*::before {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Montserrat', sans-serif;
}
</style>
