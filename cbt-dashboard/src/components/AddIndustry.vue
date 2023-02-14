<template>
    <div class="form_wrapper">
        <div class="industry_heading">Add new industry</div>
        <form class="form_inner_wrapper">
            <!--input 1--> 
            <label class="industry_label" name="" id="industry_input">
                Industry name
            </label>
            <div class="industry_required">
                <input class="industry_input" for="industry_input" type="text" required />
                <span class="dot"></span>
            </div>

            <!--input 2-->    
            <label class="industry_label" name="" id="industry_input">
                Client industry
            </label>
            <div class="industry_required">
                <input for="industry_input" class="industry_input" type="text" required />
                <span class="dot"></span>
            </div>
            <button type="submit" class="form_submit_btn">Submit</button>
        </form>
    </div>
</template>


<script>
    export default {
        name: "AddIndustry"
    }
</script>


<style lang="scss" scoped>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;1,300;1,500;1,900&display=swap');

    /*GENERAL STYLES*/
    *, 
    *::after, 
    *::before {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Montserrat', sans-serif;
    }
    .form_wrapper {
        max-width: 370px;
        width: 100%;
        display: flex;
        flex-flow: column nowrap;
        margin: 20px;
        .industry_heading {
            font-size: 1.75rem;    
            font-weight: 700;
            color: black;
            padding: 0px 0px 30px 0px;
        }

        .form_inner_wrapper {
            background-color: #80808019;
            width:100%;
            display: flex;
            flex-flow: column nowrap;
            justify-content: space-around;
            align-items: flex-start;
            padding: 25px 30px;
            border-radius: 25px;
            box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;

            .industry_label {
                color: black;
                font-size: 1rem;
                font-weight: 700;
                padding-bottom: 2px;
            }

            .industry_required {
                width:100%;
                display: flex;
                flex-wrap: nowrap;
                

                //INPUT STYLES
                .industry_input {
                    max-width: 300px;
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

                //REQUIRED FIELD DOTS
                .dot {
                    z-index: 1000;
                    height: 6px;
                    width: 6px;
                    padding-left:2px;
                    padding-right:3px;
                    background-color: red;
                    border-radius: 100%;
                    margin-left: 2px;
                    margin-right: 10px;
                }
            }


            //BUTTON STYLE
            .form_submit_btn { 
                cursor: pointer;
                align-self: flex-end;
                width:100px;
                padding: 8px 12px;
                border: none;
                color: white;
                background-color: #00CC99;
                border-radius:  5px;
                font-size: 1rem;
                box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
                margin-top: 40px;
                margin-right: 20px;

                &:hover {
                    background-color: #000000;
                    color: white;
                }
            }
        }

    }
</style>