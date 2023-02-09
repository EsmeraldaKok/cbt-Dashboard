<template>

    <div class="form_wrapper"  >
        <!--section_1-->
            <div class="section" v-show="isVisible(0)" >

            <!--Heading-->
                <div class="form_heading">
                    Section 1
                </div>

            <!--Dropdown list-->
                <div class="required">
                    <div class="user_select">
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

            <!--heading two-->
                <div class="form_subheading">
                    Project details
                </div>

            <!-----INPUTS----->
                <!--input label-->
                    <label for="projectTitle" class="user_label heading">
                        Project title
                    </label>
                <!--input-->
                    <div class="required">
                        <input type="Text" id="projectTitle" required class="user_input"/>
                        <span class="dot"></span>
                    </div>

                <!--input label-->
                    <label for="Notes" class="user_label heading">
                        Notes
                    </label>
                <!--input-->
                    <div class="required">
                        <input type="Text" id="Notes" required class="user_input" />
                        <span class="dot"></span>
                    </div>

                <!--input label-->
                    <label for="CMID" class="user_label">
                        CMID
                    </label>
                <!--input-->
                    <div class="required">
                        <input type="Text" id="CMID" required class="user_input" />
                        <span class="dot"></span>
                        <button class="form_add_btn">
                            <svg id="btn_s_circle" xmlns="http://www.w3.org/2000/svg" width="35" height="35" viewBox="0 0 40 40">
                                <circle id="Ellipse_2" data-name="Ellipse 2" cx="20" cy="20" r="20" fill="#0c9"/>
                                <path id="Path_20" data-name="Path 20" d="M26.391,24.139l6.617-6.617a1.273,1.273,0,0,0-1.8-1.8l-6.617,6.617-6.617-6.617a1.273,1.273,0,0,0-1.8,1.8l6.617,6.617-6.617,6.617a1.273,1.273,0,1,0,1.8,1.8l6.617-6.617,6.617,6.617a1.273,1.273,0,1,0,1.8-1.8Z" transform="translate(19.68 -14.458) rotate(45)" fill="#fff"/>
                            </svg>
                        </button>
                    </div>

                <!--input label-->
                    <label for="Projectdocumentvolume" class="user_label heading">
                        Project document volume
                    </label>
                <!--input-->
                    <div class="required">
                        <input type="Text" id="Projectdocumentvolume" required class="user_input" />
                        <span class="dot"></span>
                    </div>
                <!--input label-->
                    <label for="ProjecteDataCMID" class="user_label heading">
                        Project eData CMID
                    </label>
                <!--input-->
                    <div class="required">
                        <input type="Text" id="ProjecteDataCMID" required class="user_input" />
                        <span class="dot"></span>
                    </div>
                <!--right btn-->
                    <button class="form_next_btn" @click="nextSection">                  
                        Next
                    </button>
            </div>
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

        <!--section_2-->
            <div class="section" v-show="isVisible(1)" >

                <!--Heading-->
                <div class="form_heading">
                    Section 2
                </div>

                <!--heading two-->
                <div class="form_subheading">
                    Project data
                </div>

                <!-----RADIOS----->

                    <!--radio group 1-->
                    <div class="radio_wrapper">
                        <div class="required">
                            <div class="user_label_radio" name="databasePlatform" >Database Platform</div>
                            <span class="dot"></span>
                        </div>
                        <div class="radio">
                            <input type="radio" name="databasePlatform" required id="relativity" value="Relativity" class="radio_input"/>
                            <label for="Relativity" class="radio_label">Relativity</label>
                        </div>
                        <div class="radio">
                            <input type="radio" name="databasePlatform" required id="Disco" value="Disco" class="radio_input"/>
                            <label for="Disco" class="radio_label">Disco</label>
                        </div>
                        <div class="radio">
                            <input type="radio" name="databasePlatform" required id="Accelerate" value="Accelerate" class="radio_input"/>
                            <label for="Accelerate" class="radio_label">Accelerate</label>
                        </div>
                        <div class="radio">
                            <input type="radio" name="databasePlatform" required id="Other" value="Other" class="radio_input"/>
                            <label for="Other" class="radio_label">Other</label>
                        </div>
                    </div>

                    <!--radio group 2-->
                    <div class="radio_wrapper" name="scope">
                        <div class="required">
                            <div class="user_label_radio">Scope</div>
                            <span class="dot"></span>
                        </div>
                        <div class="radio">
                            <input type="radio"  name="scope" required id="Standardreview" value="Standardreview" class="radio_input"/>
                            <label for="Standardreview" class="radio_label">Standard review</label>
                        </div>
                        <div class="radio">
                            <input type="radio"  name="scope" required id="Other" value="Other" class="radio_input"/>
                            <label for="Other" class="radio_label">Other</label>
                        </div>
                    </div>

                    <!--radio group 3-->
                    <div class="radio_wrapper">
                        <div class="required">
                            <div class="user_label_radio" name="foreignLang">Has foreign language?</div>
                            <span class="dot"></span>
                        </div>
                        <div class="radio">
                            <input type="radio" required id="No" value="No" class="radio_input" name="foreignLang"/>
                            <label for="No" class="radio_label">No</label>
                        </div>
                        <div class="radio">
                            <input type="radio" required id="Yes" value="Yes" class="radio_input" name="foreignLang"/>
                            <label for="Yes" class="radio_label">Yes</label>
                        </div>
                    </div>

                <!-----INPUTS----->
                    <!--input label-->
                    <label for="startDate" class="user_label heading">
                        Start date
                    </label>
                    <div class="required">
                        <input type="date" id="startDate" required class="user_input" placeholder="Pick a date"/>
                        <span class="dot"></span>
                    </div>

                    <!--input label-->
                    <label for="dueDate" class="user_label heading">
                        Due date
                    </label>
                    <div class="required">
                        <input type="date" id="dueDate" required class="user_input" placeholder="Pick a date"/>
                        <span class="dot"></span>
                    </div>

                    <!--input label-->
                    <label for="conflictParties" class="user_label heading">
                        Conflict parties
                    </label>
                    <div class="required">
                        <input type="Text" id="conflictParties" required class="user_input" />
                        <span class="dot"></span>
                        <button class="form_add_btn">
                            <svg id="btn_s_circle" xmlns="http://www.w3.org/2000/svg" width="35" height="35" viewBox="0 0 40 40">
                                <circle id="Ellipse_2" data-name="Ellipse 2" cx="20" cy="20" r="20" fill="#0c9"/>
                                <path id="Path_20" data-name="Path 20" d="M26.391,24.139l6.617-6.617a1.273,1.273,0,0,0-1.8-1.8l-6.617,6.617-6.617-6.617a1.273,1.273,0,0,0-1.8,1.8l6.617,6.617-6.617,6.617a1.273,1.273,0,1,0,1.8,1.8l6.617-6.617,6.617,6.617a1.273,1.273,0,1,0,1.8-1.8Z" transform="translate(19.68 -14.458) rotate(45)" fill="#fff"/>
                            </svg>
                        </button>
                    </div>
                    
                    <!--input label-->
                    <label for="keyContacts" class="user_label heading">
                        Key contacts
                    </label>
                    <div class="required">
                        <input type="Text" id="keyContacts" required class="user_input" />
                        <span class="dot"></span>
                        <button class="form_add_btn">
                            <svg id="btn_s_circle" xmlns="http://www.w3.org/2000/svg" width="35" height="35" viewBox="0 0 40 40">
                                <circle id="Ellipse_2" data-name="Ellipse 2" cx="20" cy="20" r="20" fill="#0c9"/>
                                <path id="Path_20" data-name="Path 20" d="M26.391,24.139l6.617-6.617a1.273,1.273,0,0,0-1.8-1.8l-6.617,6.617-6.617-6.617a1.273,1.273,0,0,0-1.8,1.8l6.617,6.617-6.617,6.617a1.273,1.273,0,1,0,1.8,1.8l6.617-6.617,6.617,6.617a1.273,1.273,0,1,0,1.8-1.8Z" transform="translate(19.68 -14.458) rotate(45)" fill="#fff"/>
                            </svg>
                        </button>
                    </div>

                    <button class="form_next_btn" @click="nextSection">                  
                        Next
                    </button>
            </div>

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
        <!--section_3-->
            <div class="section" v-show="isVisible(2)" >
            
                <!--Heading-->
                <div class="form_heading">
                    Section 3
                </div>

                <!--heading two-->
                <div class="form_subheading">
                    Final details
                </div>

                <!-----INPUTS----->
                    <!--input label-->
                    <label for="volumeOfPages" class="user_label">
                        Volume of pages
                    </label>
                    <div class="required">
                        <input type="Text" id="volumeOfPages" required class="user_input" />
                        <span class="dot"></span>
                    </div>

                    <!--input label-->
                    <label for="teamSpeed" class="user_label">
                        Team speed
                    </label>
                    <div class="required">
                        <input type="Text" id="teamSpeed" required class="user_input" />
                        <span class="dot"></span>
                    </div>

                    <!--input label-->
                    <label for="tradeMarkSubject" class="user_label heading">
                        Trade mark subject
                    </label>
                    <div class="required">
                        <input type="Text" id="tradeMarkSubject" required class="user_input" />
                        <span class="dot"></span>
                    </div>

                    <!--input label-->
                    <label for="office" class="user_label">
                        Office
                    </label>
                    <div class="required">
                        <input type="Text" id="office" required class="user_input" />
                        <span class="dot"></span>
                    </div>

                    <!--input label-->
                    <label for="softwarePlatform" class="user_label">
                        Software platform
                    </label>
                    <div class="required">
                        <input type="Text" id="softwarePlatform" required class="user_input" />
                        <span class="dot"></span>
                    </div>

                    <!--input label-->
                    <label for="areaOfLaw" class="user_label heading">
                        Area of law
                    </label>
                    <div class="required">
                        <input type="Text" id="areaOfLaw" required class="user_input" />
                        <span class="dot"></span>
                    </div>

                    <!--input label-->
                    <label for="clientSelector" class="user_label">
                        Client selector
                    </label>
                    <div class="required">
                        <input type="Text" id="clientSelector" required class="user_input" />
                        <span class="dot"></span>
                    </div>

                    <!--input label-->
                    <label for="natureOfProceedings" class="user_label heading">
                        Nature of proceedings
                    </label>
                    <div class="required">
                        <input type="Text" id="natureOfProceedings" required class="user_input" />
                        <span class="dot"></span>
                    </div>
                    
                    <button type="submit" class="form_submit_btn">Submit</button>
            </div>
    </div>

</template>

<script>
    export default {
    
        name: "AddProject",
        data() {
            return {
                options: ['Option 1', 'Option 2', 'Option 3'],
                selected: 'Select client', //heading for dropdown
                showOptions: false,
                index: 0
                
            }
        },
        methods: {
            selectOption(option) {
                this.selected = option;
                this.showOptions = false;
            },
            nextSection() {
                this.index = (this.index + 1) % 3;
            },
            isVisible(i) {
                return window.innerWidth >= 992 ? true : this.index === i;
            }
        }    
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

    //MOBILE STYLES FOR FORM
    .form_wrapper {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        flex-flow: column  nowrap;

        .next_section_btn {
            display: none;
        }

        .section {
            max-width: 430px;
            width: 100%;
            display:flex;
            flex-flow: column nowrap;

            background-color: #80808019;
            padding: 25px;
            padding-right: 15px;
            border-radius: 25px;
            box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;


            //BUTTON STYLE
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
                margin-top: 70px;
                margin-right: 20px;
                margin-bottom: 20px;
                
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
    
            //FORM HEADINGS & TEXT
            .form_heading {
                color: black;
                font-size: 1.5rem;
                font-weight: 700;
                margin-bottom: 15px;
            }

            .form_subheading {
                color: black;
                font-size: 1.188rem;
                font-weight: 700;
                margin-bottom: 15px;
                
               
            }

            .user_label {
                color: black;
                font-size: 1rem;
                font-weight: 700;
            }
            .radio_label {
                font-size: 1rem;
                color: black;
                font-weight: 300;
                padding-left: 5px;    
            }   

            //INPUT STYLES
            .required {
                max-width: 400px;
                width:100%;
                display: flex;
                flex-shrink: 0;
                flex-wrap: nowrap;
                

                //INPUT STYLES
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

            //RADIO STYLES
            .radio{
                padding-top: 10px;
                padding-bottom: 5px;
            }

            .user_label_radio {
                //padding-bottom: 1px;
                padding-top: 4px;
                font-weight: 700;
                font-size: 1rem;
            }

            //SELECT DROPDOWN STYLES
            .user_select {
                    position: relative;
                    max-width: 266px;
                    width: 100%;
                    height: 34px;
                    background-color: white;
                    border: 1px solid black;
                    border-radius: 5px;
                    margin-bottom: 15px;
                    margin-top: 10px;
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
    }

    //MQ for desktop
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