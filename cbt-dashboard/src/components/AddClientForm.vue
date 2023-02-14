<template>
        <!--form inner-->
        <div class="form_wrapper">

            <!--form section 1-->
            <div class="section" v-show="isVisible(0)">
                
                <!--Heading-->
                <div class="form_heading">
                    Section 1
                </div>

                <!--DROPDOWN-->
                <div class="client_required">
                    <div class="client_select">
                        <div class="selected-value" @click="showOptions = !showOptions">
                            {{ selected }}         
                            <span class="down-arrow">
                                <svg xmlns="http://www.w3.org/2000/svg" width="13" height="7" viewBox="0 0 13 7">
                                    <path id="Polygon_1" 
                                        data-name="Polygon 1" 
                                        d="M5.767.789a1,1,0,0,1,1.466,0L11.44,5.32A1,1,0,0,1,10.707,7H2.293A1,1,0,0,1,1.56,5.32Z" transform="translate(13 7) rotate(180)"/>
                                </svg>
                            </span>
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

                <!--subheading-->
                <div class="form_subheading">
                    Client details
                </div>

                <!-----INPUTS----->
                <!--input label-->
                <label for="clientName" class="client_label">
                    Client name  
                </label>
                <!--input-->
                <div class="client_required">
                    <input type="Text" id="ClientName" required class="client_input"/>
                    <span class="dot"></span>
                </div>

                <!--input label-->
                <label for="clientLogo" class="client_label">
                    Client logo
                </label>
                <!--input-->
                <div class="client_required">
                <div class="upload_btn_wrapper" >
                    <button class="btn"></button>
                    <input type="file" id="ClientLogo" required class="client_input" accept="image/*"/>
                </div>    
                    <span class="dot"></span>
                    <div class="form_add_btn">
                        <svg id="btn_s_circle" xmlns="http://www.w3.org/2000/svg" width="35" height="35" viewBox="0 0 40 40">
                            <circle id="Ellipse_2" data-name="Ellipse 2" cx="20" cy="20" r="20" fill="#0c9"/>
                            <path id="Path_20" data-name="Path 20" d="M26.391,24.139l6.617-6.617a1.273,1.273,0,0,0-1.8-1.8l-6.617,6.617-6.617-6.617a1.273,1.273,0,0,0-1.8,1.8l6.617,6.617-6.617,6.617a1.273,1.273,0,1,0,1.8,1.8l6.617-6.617,6.617,6.617a1.273,1.273,0,1,0,1.8-1.8Z" transform="translate(19.68 -14.458) rotate(45)" fill="#fff"/>
                        </svg>
                    </div>
                </div>

                <!--right btn-->
                <button class="form_next_btn" @click="nextSection">                  
                    Next
                </button>

            </div>

            <!--Next arrow icon-->
            <div class="next_section_btn">
                <svg id="Group_1095" data-name="Group 1095" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="28" height="28" viewBox="0 0 28 28">
                    <defs>
                        <clipPath id="clip-path">
                        <rect id="Rectangle_635" data-name="Rectangle 635" width="28" height="28" fill="#5a5a5a"/>
                        </clipPath>
                    </defs>
                    <g id="Group_1094" data-name="Group 1094" clip-path="url(#clip-path)">
                        <path id="Path_1983" data-name="Path 1983" d="M14,0A14,14,0,1,0,28,14,14,14,0,0,0,14,0m5.04,15.01L12.8,21.25a1.35,1.35,0,0,1-.94.39,1.315,1.315,0,0,1-.93-2.25L16.32,14,10.93,8.61a1.315,1.315,0,0,1,.93-2.25,1.292,1.292,0,0,1,.94.39l6.24,6.24a1.424,1.424,0,0,1,0,2.02" fill="#5a5a5a"/>
                    </g>
                </svg>
            </div>

            <!--form section 2-->
            <div class="section" v-show="isVisible(1)">

                <!--Heading-->
                <div class="form_heading">
                    Section 2
                </div>

                <!-----INPUTS----->
                <!--input label-->
                <label for="clientEmail" class="client_label">
                    Email address 
                </label>
                <!--input-->
                <div class="client_required">
                    <input type="Email" id="clientEmail" required class="client_input"/>
                    <span class="dot"></span>
                </div>

                <!--input label-->
                <label for="clientNumber" class="client_label">
                    Contact Number
                </label>
                <!--input-->
                <div class="client_required">
                    <input type="tel" id="clientNumber" required class="client_input"/>
                    <span class="dot"></span>
                </div>

                <!--right btn-->
                <button class="form_next_btn" @click="nextSection">                  
                    Next
                </button>
            </div>

            <!--Next arrow icon-->
            <div class="next_section_btn">
                <svg id="Group_1095" data-name="Group 1095" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="28" height="28" viewBox="0 0 28 28">
                    <defs>
                        <clipPath id="clip-path">
                        <rect id="Rectangle_635" data-name="Rectangle 635" width="28" height="28" fill="#5a5a5a"/>
                        </clipPath>
                    </defs>
                    <g id="Group_1094" data-name="Group 1094" clip-path="url(#clip-path)">
                        <path id="Path_1983" data-name="Path 1983" d="M14,0A14,14,0,1,0,28,14,14,14,0,0,0,14,0m5.04,15.01L12.8,21.25a1.35,1.35,0,0,1-.94.39,1.315,1.315,0,0,1-.93-2.25L16.32,14,10.93,8.61a1.315,1.315,0,0,1,.93-2.25,1.292,1.292,0,0,1,.94.39l6.24,6.24a1.424,1.424,0,0,1,0,2.02" fill="#5a5a5a"/>
                    </g>
                </svg>
            </div>

            <!--form section 3-->
            <div class="section" v-show="isVisible(2)">

                <!--Heading-->
                <div class="form_heading">
                    Section 3
                </div>

                <!---INPUT 1--->
                <label for="color1" class="client_label">
                    Primary colour
                </label>
                <!--input-->
                <div class="client_required">
                    <input type="text" :name="'color-' + 0" v-model="colors[0]" v-on:input="updateColor(0)" class="client_input" />
                    <div class="color_box" :style="{ backgroundColor: colors[0] }"></div>
                </div>
                <!-- INPUT 2 -->
                <label for="color2" class="client_label">
                    Secondary colour
                </label>
                <!--input-->
                <div class="client_required">
                    <input type="text" :name="'color-' + 1" v-model="colors[1]" v-on:input="updateColor(1)" class="client_input" />
                    <div class="color_box" :style="{ backgroundColor: colors[1] }"></div>
                </div>

                <!-- INPUT 3 -->
                <label for="color3" class="client_label">
                    Scaffold colour
                </label>
                <!--input-->
                <div class="client_required">
                    <input type="text" :name="'color-' + 2" v-model="colors[2]" v-on:input="updateColor(2)" class="client_input" />
                    <div class="color_box" :style="{ backgroundColor: colors[2] }"></div>
                </div>

                <!-- INPUT 4 -->
                <label for="color3" class="client_label">
                    AppBar colour
                </label>
                <!--input-->
                <div class="client_required">
                    <input type="text" :name="'color-' + 3" v-model="colors[3]" v-on:input="updateColor(3)" class="client_input" />
                        <div class="color_box" :style="{ backgroundColor: colors[3] }"></div>
                </div>

                <!--SUBMIT BTN-->
                <button type="submit" class="form_submit_btn">
                    Submit
                </button>
            </div>
        </div>

</template>

<script>

export default {
    
    name: "AddClientForm",
    data() {
        return {
            options: ['Option 1', 'Option 2', 'Option 3'],
            selected: 'Client type', //heading for dropdown
            showOptions: false,
            index: 0,
            colors: ['#001100', '#000000', '#000000', '#000000']
        }
    },
    methods: {
        //dropdown
        selectOption(option) {
            this.selected = option;
            this.showOptions = false;
        },
        //page sections
        nextSection() {
            this.index = (this.index + 1) % 3;
        }, 
        //desktop view
        isVisible(i) {
            return window.innerWidth >= 992 ? true : this.index === i;
        },
        //color picker
        updateColor(index) {
            if (/^#[0-9a-fA-F]{6}$/.test(this.colors[index])) {
                this.$set(this.colors, index, this.colors[index]);
            }
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

    //MOBILE STYLES

    //display none 
    .next_section_btn {
        display: none;
    }

    .form_wrapper {
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        flex-flow: column nowrap;

        .section {
            max-width: 370px;
            width: 100%;
            display:flex;
            flex-flow: column nowrap;
            background-color: #80808019;
            padding: 25px;
            padding-right: 15px;
            border-radius: 25px;
            box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;

            //form heading
            .form_heading {
                color: black;
                font-size: 1.5rem;
                font-weight: 700;
                margin: 0px 9px 20px 0px;

                
            }
        
            .form_subheading {
                color: black;
                font-size: 1.188rem;
                font-weight: 700;
                margin-top: 15px;
                margin-bottom: 10px;
            }
            
            .client_label {
                color: black;
                font-size: 1rem;
                font-weight: 700;
                padding-bottom: 3px;
            }

            //buttons
            .form_submit_btn,
            .form_next_btn { 
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
                margin: 40px 0px 0px 40px;
                
                &:hover {
                    background-color: #000000;
                    color: white;
                }
            }
            .form_add_btn {
                cursor: pointer;
                border: none;
                padding-right: 10px;
                justify-self: flex-end;
                margin-bottom: 5px;
                background-color: transparent;
                position: relative;
    
                svg:hover circle {
                    fill: black;
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
                //margin-top: 10px;
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

            //input
            .client_required {
                max-width: 370px;
                width:100%;
                display: flex;
                flex-shrink: 0;
                flex-wrap: nowrap;
                

                //INPUT STYLES
                .client_input {
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

                .color_box {
                    width: 34px;
                    height: 34px;
                    margin-left: 10px;
                    border-radius: 5px;
                }

                .upload_btn_wrapper {
                    position: relative;
                    overflow: hidden;
                    display: flex;
                    .btn {
                        
                        border: 1px solid black;
                        color: gray;
                        background-color: white;
                        width: 266px;
                        
                        height: 34px;
                        border-radius: 5px;
                        font-size: 20px;
                        font-weight: bold;
                    }


                }
                .upload_btn_wrapper input[type=file] {
                    font-size: 100px;
                    position: absolute;
                    left: 0;
                    top: 0;
                    opacity: 0;
                }
            }  

        }

    }

    //MQ DESKTOP

    @media only screen and (min-width: 929px) {
        .form_wrapper{
                flex-flow: row nowrap;
                align-items: flex-start;
                justify-content: space-evenly;
                background-color: #80808019;
                border-radius: 25px;
                box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
                //max-width: 1400px;
                //width: 100%;
                
                .section {
                    width: calc(100% / 3);
                    background-color: transparent;
                    box-shadow: none;
                    border-radius: 0;
                }

                .form_next_btn {
                    display: none;
                }

                .next_section_btn {
                    display: block;
                    align-self: center;
                    justify-self: center;
                    margin-right: 10px;
                    margin-left: 10px;
                }
            }
    }
</style>