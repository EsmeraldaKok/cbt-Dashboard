<template>
    <div class="form_section_two">
        <div class="form_section_two_heading">
            Section 2
        </div>
        <div class="form_section_two_subheading">
            Project data
        </div>
        <div class="form_section_two_radio_wrapper">
            <div class="form_section_two_radio_wrapper_heading">Database platform</div>
            <div class="radio">
                <input type="radio" required id="relativity" value="Relativity" class="radio_input"/>
                <label for="Relativity" class="radio_input_label">Relativity</label>
            </div>
            <div class="radio">
                <input type="radio" required id="Disco" value="Disco" class="radio_input"/>
                <label for="Disco" class="radio_input_label">Disco</label>
            </div>
            <div class="radio">
                <input type="radio" required id="Accelerate" value="Accelerate" class="radio_input"/>
                <label for="Accelerate" class="radio_input_label">Accelerate</label>
            </div>
            <div class="radio">
                <input type="radio" required id="Other" value="Other" class="radio_input"/>
                <label for="Other" class="radio_input_label">Other</label>
            </div>
        </div>
        <div class="form_section_two_radio_wrapper">
            <div class="form_section_two_radio_wrapper_heading">Scope</div>
            <div class="radio">
                <input type="radio" required id="Standardreview" value="Standardreview" class="radio_input"/>
                <label for="Standardreview" class="radio_input_label">Standard review</label>
            </div>
            <div class="radio">
                <input type="radio" required id="Other" value="Other" class="radio_input"/>
                <label for="Other" class="radio_input_label">Other</label>
            </div>
        </div>
        <div class="form_section_two_radio_wrapper">
            <div class="form_section_two_radio_wrapper_heading">Has foreign language?</div>
            <div class="radio">
                <input type="radio" required id="No" value="No" class="radio_input"/>
                <label for="No" class="radio_input_label">No</label>
            </div>
            <div class="radio">
                <input type="radio" required id="Yes" value="Yes" class="radio_input"/>
                <label for="Yes" class="radio_input_label">Yes</label>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "AddProjectFormS2"
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
    
    .form_section_two {
        max-width: 340px;
        width: 100%;
        display: flex;
        flex-flow: column nowrap;
        background-color: #80808019;
        border-radius: 15px;
        padding: 20px 30px;

        &_heading {
            font-size: 1.5rem;
            font-weight: 700;
            color: black;
            margin-bottom: 20px;
        }

        &_subheading {
            font-size: 1.188rem;
            font-weight: 700;
            color: black;
        }
        &_radio_wrapper {
            display: flex;
            flex-flow: column nowrap; 
            margin: 10px;
            
            &_heading{
                font-size: 1rem;
                font-weight: 700;
                color:black;
            }
            
            .radio {
                padding:  8px 0px 0px 0px;

                input[type="radio"] {
                    position: absolute;
                    opacity: 0;

                    & + label {
                        position: relative;
                        cursor: pointer;
                        padding-left: 25px;
                        font-size: 1rem;
                    }

                    & + label:before {
                        content: "";
                        position: absolute;
                        left: 0;
                        top: 0;
                        width: 15px;
                        height: 15px;
                        border: 1px solid black;
                        border-radius: 100%;
                        background: white;

                        &:checked {
                            border: 1px solid rgb(20, 201, 214);
                        }
                    }

                    &:checked + label:after {
                        content: "";
                        position: absolute;
                        left: 3.8px;
                        top: 3.8px;
                        width: 8px;
                        height: 8px;
                        border-radius: 100%;
                        background: rgb(20, 201, 214);
                    }
                }
            }
        }
    }
</style>