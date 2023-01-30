<template>
  <div id="app">
    <!--<UserInfo />-->
    <!--<UserTable />-->
    <!--<AddProjectFormS1 />-->
    <AddUser />
  </div>
</template>

<script>

//import UserInfo from './components/UserInfo.vue';
//import UserTable from './components/UserTable.vue';
import AddUser from './components/AddUser.vue';

//import AddProjectFormS1 from './components/AddProjectFormS1.vue';

export default {
    name: "App",
    components: { AddUser }
}
</script>

<style lang="scss" scoped>
  .user_select {
            position: relative;
            max-width: 266px;
            width: 100%;
            height: 34px;
            background-color: white;
            border: 1px solid black;
            border-radius: 5px;
            margin-bottom: 15px;
            
            .selected-value {
                padding: 5px 5px;
                text-align: left; 
                cursor: pointer;
                font-size: 1rem;
                color: black;
                font-weight: 700;
            }

            .options {
                position: absolute;
                top: calc(100% + 3px);
                left: 0;
                width: 100%;
                max-height: 200px;
                overflow-y: scroll;
                background: linear-gradient(284deg, rgba(255, 255, 255, 0.986) 45%, rgba(223, 223, 223, 0.986) 92%);
                border-radius: 5px;
                overflow-y: hidden;

                .option {
                    color: black;
                    padding: 5px;
                    font-size: 1rem;
                    font-weight: 300;
                    cursor: pointer;
                    

                    &:hover {
                        background-color: #00CC99;
                        color: white;
                    }
                }
            }
        }
</style>
