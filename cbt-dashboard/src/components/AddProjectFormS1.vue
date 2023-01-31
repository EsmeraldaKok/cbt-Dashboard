<template lang="HTML5">
    <div class="form_section_one">
        <!--heading one-->
        <div class="form_section_one_heading">
            Section 1
        </div>

        <!--dropdown-->
        <div class="client_select">
            <div class="selected-value" @click="showOptions = !showOptions">
                {{ selected }}
            </div>
            <div class="options" v-show="showOptions">
            <div class="option" v-for="(option, index) in options" :key="index" 
                @click="selectOption(option)">
                {{ option }}
            </div>
            </div>
        </div>
	
        <!--heading two-->
        <div class="form_section_one_headingTwo">
            Project details
        </div>
        <label class="form_section_one_InputHeading">Project title</label>
        <input type="text" required class="input_wrapper" />
        <label class="form_section_one_InputHeading">Notes</label>
        <input type="text" class="input_wrapper" />
        <label class="form_section_one_InputHeading">CMID</label>
        <input type="text" required class="input_wrapper" />
        <label class="form_section_one_InputHeading">Project document volume</label>
        <input type="text" required class="input_wrapper" />
        <label class="form_section_one_InputHeading">Project eData CMID</label>
        <input type="text" required class="input_wrapper" />

    </div>
</template>



<script>
    export default {
        name: "AddProjectFormS1",
        data() {
            return {
            options: ['Option 1', 'Option 2', 'Option 3'],
            selected: 'Choose client', //heading for dropdown
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
    
    .form_section_one {
        max-width: 340px;
        width: 100%;
        display: flex;
        flex-flow: column nowrap;
        justify-content: space-evenly;
        align-items: left;
        background-color: #80808019;
        border-radius: 15px;
        padding: 20px 30px;

        //heading styles
        &_heading {
            font-size: 1.5rem;
            font-weight: 700;
            color: black;
            margin-bottom: 20px;
        }

        &_headingTwo {
            font-size: 1.188rem;
            font-weight: 700;
            color: black;
            margin-bottom: 10px;
        }

        &_InputHeading {
            font-size: 1rem;
            font-weight: 700;
            color: black;
        }

        //input styles
        .input_wrapper {
            max-width: 266px;
            width: 100%;
            outline: none;
            border-radius: 5px;
            border: 1px solid black;
            height:34px;
            font-size: 1rem;
            font-weight: 300;
            color: black;
            padding: 8px;
            margin-bottom: 10px;
        }
    }
        //dropdown

        .client_select {
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
    }

</style>