<template> 
    <form class="user_wrapper">
    <div class="required">
        <div class="user_select">
            <div class="selected-value" @click="showOptions = !showOptions">
                {{ selected }}         <span class>▼</span>
            </div>
            <div class="options" v-show="showOptions">
            <div class="option" v-for="(option, index) in options" :key="index" 
                @click="selectOption(option)">
                {{ option }}
            </div>
            </div>
        </div>
        <span class="dot"></span>
    </div>
         <!--Heading -->
        <div class="user_heading">User details</div>

        <label for="Fullname" class="user_label">Full name</label>
        <div class="required">
            <input type="Text" id="Fullname" required class="user_input" />
            <span class="dot"></span>
        </div>

        <label for="username" class="user_label">Username</label>
        <div class="required">
            <input id="username" required type="text" class="user_input required" />
            <span class="dot"></span>
        </div>

        <label for="email" class="user_label">Email address</label>
        <div class="required">
            <input id="email" required type="email" class="user_input required" />
            <span class="dot"></span>
        </div>

        <label for="password" class="user_label">Password</label>
        <div class="required">
            <input type="password" required class="user_input required" />
            <span class="dot"></span>
        </div>

        <label for="password" class="user_label">Confirm password</label>
        <div class="required">
            <input type="password" required class="user_input required" />
            <span class="dot"></span>
        </div>
        <button type="submit" class="user_submit_btn">Submit</button>
    </form>
</template>

<script>

   export default {
    name: "AddUser",
    data() {
            return {
            options: ['Option 1', 'Option 2', 'Option 3'],
            selected: 'Select client', //heading for dropdown
            showOptions: false
            }
        },
        methods: {
            selectOption(option) {
            this.selected = option;
            this.showOptions = false;
            }
        }
    }
   
</script>



<style lang="scss" scoped>

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

    .user_wrapper {
        max-width: 330px;
        width: 100%;
        display: flex;
        flex-flow: column nowrap;
        background-color: #8f8f8f29;
        border-radius: 25px;
        padding: 30px 40px;
        justify-content: center;

        //Input styles     
        .required {
            max-width: 285px;
            width:100%;
            display: flex;
            flex-wrap: nowrap;
            justify-content: space-between;
            padding: 2px;
            
            .user_input {
                max-width: 266px;
                width:100%;
                height: 34px;
                border: 1px solid #000000;
                border-radius: 5px;
                margin-bottom:15px;
                color: black;
                font-size: 1rem;
                font-weight: 300;
                padding-left: 10px;
                
            }
            .dot {
                height: 6px;
                width: 6px;
                background-color: red;
                border-radius: 100%;
                margin-left: 3px;
            }

    }

        //input label styles
        .user_label {
            font-size: 1rem;
            font-weight: 700;
            color: black;
        }

        //button styling
        .user_submit_btn {
            align-self: flex-end;
            width:100px;
            padding: 8px 12px;
            border: none;
            color: white;
            background-color: #00CC99;
            border-radius:  5px;
            font-size: 1rem;
            box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
            margin-top: 25px;

            &:hover {
                background-color: black;

            }
        }

        //heading styling
        .user_heading {
            font-size: 1.188rem;
            color: black;
            font-weight: 700;
            margin-bottom: 20px;
        }
        
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
            display: flex;
            justify-content: space-between;
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
                background: linear-gradient(284deg, rgba(255, 255, 255, 0.986) 45%, rgba(228, 228, 228, 0.986) 92%);
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
    }
</style>