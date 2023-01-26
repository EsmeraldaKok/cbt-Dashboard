<template>

    <div class="user_table_wrapper">

        <!--desktop view headings-->
        <div class="grid_wrapper_heading ">
            <div class="grid_wrapper_heading" role="columnheader">Client</div>
            <div class="grid_wrapper_heading" role="columnheader">Name</div>
            <div class="grid_wrapper_heading" role="columnheader">Surname</div>
            <div class="grid_wrapper_heading" role="columnheader">Email</div>
            <div class="grid_wrapper_heading" role="columnheader">Created</div>
            <div class="grid_wrapper_heading" role="columnheader">Action</div>
        </div>

        <!-- desktop view data-->
        <div class="grid_wrapper_data desktop_table" role="rowgroup" v-for="(item, index) in items" :key="index">
            <!--Client-->
            <div class="grid_wrapper_data client" role="cell">
                {{ companyName }}
            </div>

            <!--Name-->
            <div class="grid_wrapper_data surname" role="cell">
                {{ item.surname }}
            </div>

            <!--Surname-->
            <div class="grid_wrapper_data name" role="cell">
                {{ item.name }}
            </div>

            <!--Email-->
            <div class="grid_wrapper_data email" role="cell">
                {{ item.email }}
            </div>
            
            <!--Date Created-->
            <div class="grid_wrapper_data created" role="cell">
                {{ item.date_created }}
            </div>

            <!--Desktop Button Group-->
            <div class="grid_wrapper_data action" role="cell">
                <button class="action_btns_view btn_action">View</button>
                <button class="action_btns_edit btn_action">Edit</button>
                <button class="action_btns_delete btn_action">Delete</button>
            </div> 
        </div>

        <!--mobile view data-->
        <div class="wrapper_info" id="WrapperInfo" v-for="(item, index) in items" :key="index">
               
            <!--user info-->
            <div class="wrapper_info_inner">
            
                <!--Client-->
                <div class="wrapper_info_client">
                    {{ companyName }}
                </div>
                <!--Fullname-->
                <div class="wrapper_info_fullname">
                        {{ item.surname }}, {{ item.name }}
                </div>
                <!--Name-->
         
                <!--Email-->
                <div class="wrapper_info_email">
                    {{ item.email }}
                </div>
                <br />
                <!--Date Created-->
                <div class="wrapper_info_created">
                    {{ item.date_created }}
                </div>
            </div>

            <!--mobile view buttons-->
            <div class="wrapper_btn">
                <button class="btn">
                    <svg xmlns="http://www.w3.org/2000/svg" 
                        width="20" 
                        height="20" 
                        viewBox="0 0 7.991 16">
                        <path id="Path_8" 
                            data-name="Path 8" 
                            d="M1297.142,527a1,1,0,0,1-.757-1.656l5.429-6.283-5.435-6.412a1,1,0,0,1,1.527-1.295l5.989,7.066a1,1,0,0,1-.006,1.3l-5.989,6.932A1,1,0,0,1,1297.142,527Z" 
                            transform="translate(-1296.141 -511)" 
                            fill="#00C2D6"/>
                    </svg>
                </button>
            </div>
        </div>
    </div>   

</template>

<script>

    //fake data
    let items = [
        {"name": "Harland",

        "surname": "Sander",

        "email": "email@email.com",

        "date_created": "2022/01/17",

        "notes": "some note"},

        {"name": "Harland",

        "surname": "Sander",

        "email": "email@email.com",

        "date_created": "2022/01/17",

        "notes": "some note"},

        {"name": "Harland",

        "surname": "Sander",

        "email": "email@email.com",

        "date_created": "2022/01/17",

        "notes": "some note"},

        {"name": "SCOOBYDOO",

        "surname": "Sander",

        "email": "email@email.com",

        "date_created": "2022/01/17",

        "notes": "some note"},

        {"name": "ujtyhrtgeRF",

        "surname": "Sander",

        "email": "email@email.com",

        "date_created": "2022/01/17",

        "notes": "k,hjmhgf"}

    ]

    export default {
        name: "UserTable",
        data() {
            return {
                "items": items,
                companyName: "KFC",
            }
        }
    }
</script>

<style lang="scss" scoped>

    /*Style variables */
    $cbt-red: #F52F57;
    $cbt-blue: #00C2D6;
    $cbt-purple: #96008B;
    $cbt-yellow: #FDCA01;
    $cbt-green: #00CC99;
    $cbt-dark-background: #2F313E;
    $cbt-light-background: #80808015;

    /*google font */
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,300;0,400;0,600;1,500&display=swap');
    
    /* general  styles*/
    *, 
    *::after, 
    *::before {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Monserrat', sans-serif;
    }

    /* Hidden elements in mobile view */
    .grid_wrapper_heading,
    .grid_wrapper_data {
        display: none;
    }

    .user_table_wrapper {
            display: grid;
            grid-template-columns: repeat(1, 1fr);
            grid-template-rows: auto;
            row-gap:4px;
            column-gap: 4px;
 
            .wrapper_info {
                display: flex;
                justify-content: space-between;
                border: 1px solid #e8e8e8a8;
                border-radius: 15px;
                padding: 5px;

                &_client {
                    padding: 5px;
                    font-size: 1.188rem;
                    font-weight: 700;
                    color: black;
                }

                &_fullname {
                    padding: 5px 3px;
                    font-size: 0.75rem;
                    font-weight: 600;
                }

                &_email {
                    padding: 5px;
                    font-size: 0.75rem;
                    font-style: italic; /*italic email bold */
                }
                &_created {
                    padding: 5px;
                    font-size: 0.75rem;
                }
                .wrapper_btn {
                    align-self: center;
                    .btn {
                        cursor: pointer;
                        padding:15px 5px; 
                        border: none;
                        background-color: transparent;
                    }
                }
            }
    }

/* MEDIA QUERIES*/

    /* MEDIUM SCREENS */
        @media only screen and (min-width: 480px) {
            .user_table_wrapper {
                grid-template-columns: repeat(2, minmax(200px,390px));
            }
        }

        @media only screen and (min-width: 756px) {
            .user_table_wrapper {
                grid-template-columns: repeat(3, minmax(250px,1fr));
            }
        }

    /* LARGE SCREENS */
        @media only screen and (min-width: 1200px) {

            .wrapper_btn,
            .grid_wrapper_info_fullname,
            #WrapperInfo,
            .wrapper_info_inner {
                display: none;
            }
            .user_table_wrapper {
                background-color: #00000029;
                border-radius: 15px;
                display: block;
                padding: 4px;

                /* wrappers grid layout */
                .grid_wrapper_heading,
                .grid_wrapper_data {
                    display: grid;
                    grid-template-columns: repeat(6, 1fr) ;
                    grid-template-rows: auto;
                    align-items: center;
                }

                /* Heading wrapper */
                .grid_wrapper_heading {
                    color: black;
                    font-size: 1.125rem;
                    font-weight: 800;
                    margin: 2px 5px;
                }

                /* Data Wrapper */
                .grid_wrapper_data {
                    color: black;
                    font-size: 1rem;
                    line-height: 19px;
                    font-weight: 300;
                    margin: 2px 5px;
                    border: 1px solid transparent;  
                    
                    
                    .action {
                        display: flex;
                        /* All button styles */
                        .btn_action{
                            font-size: 0.75rem;
                            font-weight: 500;
                            border-radius: 40px;
                            padding: 6px 8px;
                            border: none;
                            margin-right:10px;
                            text-align: center;
                            box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
                        }

                        &_btns_view {
                            background-color: white;
                            color:#00C2D6;
                            
                            &:hover {
                                color: black;
                            }
                            
                        }

                        &_btns_edit {
                            color: white;
                            background-color: #00C2D6;

                            &:hover {
                                color: white;
                                background-color: black;
                            }
                        }
                        
                        &_btns_delete {
                            background-color: #F52F57;
                            color: white;

                            &:hover {
                                color: white;
                                background-color: black;
                            }
                        }
                    }
                }

                /* Hover effects */
                .desktop_table:hover{
                    border: 1px solid white;
                    border-radius: 8px;
                    background-color: #ffffff9c;
                    margin: 2px 5px;
                }
            }
        }
</style> 