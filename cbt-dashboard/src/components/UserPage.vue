 <template>

<!---- SMALLER SCREENS HTML----->

    <!--GRID LAYOUT WRAPPER-->
    <div class="user_table_wrapper">

        <!--card wrapper-->
        <div class="user_table" v-for="(item, index) in items" :key="index">

            <!--User info wrapper-->
            <div class="user_wrapper">

                <!--Client-->
                <h4 class="column_info_heading">{{ companyName }}</h4>

                <!--Fullnames-->
                <span class="column_info">{{ item.name }}, {{ item.surname }}</span>

                <!--Name-->
                <div class="column_info column_info_hide">
                    <h4 class="user_column_heading">NAME</h4>
                    <span class="column_info_text "><strong>{{ item.name}}</strong></span>
                </div>

                <!--Surname-->
                <div class="column_info column_info_hide">
                    <h4 class="user_column_heading">SURNAME</h4>
                    <span class="column_info_text">{{ item.surname }}</span>
                </div>
                <!--Email-->
                <div class="column_info column_info_email">
                    <h4 class="user_column_heading">EMAIL</h4>
                    <span class="column_info_text">{{ item.email }}</span>
                </div>

                <br/>

                <!--Date created-->
                <div class="column_info">
                    <h4 class="user_column_heading">CREATED</h4>
                    <span class="column_info_text">{{ item.date_created }}</span>
                </div>

                <!--Notes-->
                <div class="column_info column_info_notes">
                    <h4 class="user_column_heading">NOTES</h4>
                    <span class="column_info_text">{{ item.notes }}</span>
                </div>
                
            </div>

            <!--Button Wrapper-->
            <div class="user_btn_wrapper">
                <button class="column_btn">
                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 7.991 16">
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


<!---- DESKTOP SCREENS HTML----->
    <div  class="user_table_container">
        <!--Table header-->
        <div class="user_grid_table" role="rowgroup">
            <h5 class="User_grid_table_row_heading" role="columnheader">Client</h5>
            <div class="User_grid_table_row_heading" role="columnheader">Name</div>
            <div class="User_grid_table_row_heading" role="columnheader">Surname</div>
            <div class="User_grid_table_row_heading" role="columnheader">Email</div>
            <div class="User_grid_table_row_heading" role="columnheader">Created</div>
            <div class="User_grid_table_row_heading" role="columnheader">Action</div>
        </div>

        <!--Table rows-->
        <div class="user_grid_table row" role="rowgroup" v-for="(item, index) in items" :key="index">
            <div class="grid_user_row_info client" role="cell">{{ companyName }}</div>
            <div class="grid_user_row_info name" role="cell">{{ item.surname }}</div>
            <div class="grid_user_row_info surname" role="cell">{{ item.name }}</div>
            <div class="grid_user_row_info email" role="cell">{{ item.email }}</div>
            <div class="grid_user_row_info created" role="cell">{{ item.date_created }}</div>
            <div class="grid_user_row_info action" role="cell">
                <button class="action_btns_view">view</button>
                <button class="action_btns_edit">Edit</button>
                <button class="action_btns_delete">Delete</button>
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

        {"name": "Harland",

        "surname": "Sander",

        "email": "email@email.com",

        "date_created": "2022/01/17",

        "notes": "some note"},

        {"name": "Harland",

        "surname": "Sander",

        "email": "email@email.com",

        "date_created": "2022/01/17",

        "notes": "some note"}

    ]

    export default {
        name: "UserPage",
        data() {
            return {
                "items": items,
                companyName: "KFC",
            }
        }
    }
</script>

<style lang="scss" scoped>

    /*google font */
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,300;0,400;0,600;1,500&display=swap');
    
    /* general  styles*/
    *, 
    *::after, 
    *::before {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'monserrat', sans-serif;
    }

    /* hidden elemets */
    .user_table_header,
    .user_column_heading,
    .column_info_notes,
    .user_grid_table,
    .column_info_hide {
        display: none;
    }

    /*main grid wrapper */
    .user_table_wrapper {
        max-width: 392px;
        width: 100%;
        display: grid;
        grid-template-columns: repeat(1, 1fr);
        grid-template-rows: auto;
        row-gap:4px;
        column-gap: 8px;
    }

    /* card wrapper*/
    .user_table {
        display: flex;
        justify-content: space-between;
        border: 1px solid #e8e8e8a8;
        border-radius: 15px;
        padding: 5px;
    }
    .user_wrapper {
        padding: 10px;
    }
    /*button layout */
    .user_btn_wrapper {
        align-self: center;
    }
    /*button styling */
    .column_btn {
        cursor: pointer;
        padding: 15px 8px;
        outline: none;
        border:none;
        background-color: transparent;
    }

    /* card info styling */
    .column_info:first-of-type {
        font-size: 12px;   /*making fullname bold */
        font-weight: 600;
    }

    .column_info_email {
        font-style: italic; /*italic email bold */
    }
    
    .column_info_heading {
        font-size: 19px;
        color: black;
    }
    .column_info_text {
        text-align: left;
        font-size:12px;
    }

/* MEDIA QUERIES*/

    /* MEDIUM SCREENS */
    @media only screen and (min-width: 600px) {
        /*main grid wrapper */
        .user_table_wrapper {
            width: 392px;
            max-width: 100%;
            display: grid;
            grid-template-columns: repeat(3, minmax(340px, 1fr));
            grid-template-rows: auto;
            column-gap: 8px;
            row-gap: 8px;
        }
    }

    /* LARGE SCREENS */
    @media only screen and (min-width: 1080px) {

        /*main grid wrapper Hide smaller screen html */
        .user_table_wrapper {
            display: none;
        }
        .user_table_container {
            background-color: #E8E8E8;
            border-radius: 15px;
            padding: 14px;
            
            .user_grid_table {
                display:grid;
                grid-template-columns: repeat(7, minmax(154px, 1fr));
                column-gap: 5px;
                row-gap: 2px;

                &:hover{
                    border: 1px solid white;
                    border-radius: 8px;
                    background-color: rgba(255, 255, 255, 0.61);
                }

                .User_grid_table_row_heading{
                    font-size: 18px;
                    font-weight: bold;
                    padding: 4px 0px 4px 0px;
                }

                .grid_user_row_info {
                    font-size: 15.5px;
                    font-weight: 300;
                    line-height: 19px;
                    padding: 5px 0px 5px 1.5px;

                    .action {
                        max-width: 217px;
                        width:100%;
                        
                        &_btns_view {
                            cursor: pointer;
                            background-color: white;
                            border: none;
                            color:#00C2D6;
                            padding: 3px 5px;
                            border-radius: 25px;
                            margin-right: 4px;
                            box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;

                            &:hover {
                                color: black;
                            }
                        }

                        &_btns_edit {
                            cursor: pointer;
                            color: white;
                            border: none;
                            background-color:#00C2D6;
                            padding: 3px 6px;
                            border-radius: 25px;
                            margin-right: 4px;
                            box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;

                            &:hover {
                                background-color: black;
                            }
                        }

                        &_btns_delete {
                            cursor: pointer;
                            color: white;
                            border: none;
                            background-color:#F52F57;
                            padding: 3px 6px;
                            border-radius: 25px;
                            margin-right: 4px;
                            box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;

                            &:hover {
                                background-color: black;
                            }
                        }


                    }
                }
            }
        }    
    }

</style>