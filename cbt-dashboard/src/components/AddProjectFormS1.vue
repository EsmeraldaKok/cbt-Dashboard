<template lang="HTML5">
    <div class="form_section_one">
        <!--heading one-->
        <div class="form_section_one_heading">
            Section 1
        </div>

        <!--dropdown-->
        <select name="clients" id="client" class="input_wrapper dropdown">
            <option value="select">Choose Client</option>
            <option value="option 1">Option 1</option>
            <option value="option 2">Option 2</option>
        </select>  
	
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
        padding: 20px;

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

            option {
                background: #FFFFFF00 0% 0% no-repeat padding-box;
                box-shadow: 0px 3px 6px #00000029;                border-radius: 5px;
                opacity: 1;
                backdrop-filter: blur(30px);
                -webkit-backdrop-filter: blur(30px);

                &:hover {
                    color: white;
                    box-shadow: 0 0 10px 100px green inset;
                }
            }

        }
        .dropdown {

            outline: 0;
            background: white;
            color: black;
            font-weight:700 ;
            font-size: 16px;
            option {
                background: #FFFFFF00 0% 0% no-repeat padding-box;
                box-shadow: 0px 3px 6px #00000029;                
                border-radius: 5px;
                opacity: 1;
                backdrop-filter: blur(30px);
                -webkit-backdrop-filter: blur(30px);

                &:hover {
                    color: white;
                    box-shadow: 0 0 10px 100px green inset;
                }
            }
        }
    }
</style>