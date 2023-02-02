<template>
    <div class="form_wrapper">

        <!----Mobile---->

        <div v-if="isMobileView">
        <!--section_1-->
            <div class="section" v-if="showElement === 1">

                <!--Heading-->
                <div class="form_heading">
                    Section 1
                </div>

                <!--Dropdown list-->
                <div class="required">
                    <div class="user_select">
                        <div class="selected-value" @click="showOptions = !showOptions">
                            {{ selected }}         <span class="down-arrow">▼</span>
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
            </div>

        <!--right btn-->
            <button class="form_next_btn" v-if="showButton === 1" @click="toggleShowElement">                    
                Next
            </button>
        
        <!--section_2-->
            <div class="section" v-if="showElement === 2">

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
                            <div class="user_label">Database Platform</div>
                            <span class="dot"></span>
                        </div>
                        <div class="radio">
                            <input type="radio" required id="relativity" value="Relativity" class="radio_input"/>
                            <label for="Relativity" class="radio_label">Relativity</label>
                        </div>
                        <div class="radio">
                            <input type="radio" required id="Disco" value="Disco" class="radio_input"/>
                            <label for="Disco" class="radio_label">Disco</label>
                        </div>
                        <div class="radio">
                            <input type="radio" required id="Accelerate" value="Accelerate" class="radio_input"/>
                            <label for="Accelerate" class="radio_label">Accelerate</label>
                        </div>
                        <div class="radio">
                            <input type="radio" required id="Other" value="Other" class="radio_input"/>
                            <label for="Other" class="radio_label">Other</label>
                        </div>
                    </div>

                    <!--radio group 2-->
                    <div class="radio_wrapper">
                        <div class="required">
                            <div class="user_label">Scope</div>
                            <span class="dot"></span>
                        </div>
                        <div class="radio">
                            <input type="radio" required id="Standardreview" value="Standardreview" class="radio_input"/>
                            <label for="Standardreview" class="radio_label">Standard review</label>
                        </div>
                        <div class="radio">
                            <input type="radio" required id="Other" value="Other" class="radio_input"/>
                            <label for="Other" class="radio_label">Other</label>
                        </div>
                    </div>

                    <!--radio group 3-->
                    <div class="radio_wrapper">
                        <div class="required">
                            <div class="user_label">Has foreign language?</div>
                            <span class="dot"></span>
                        </div>
                        <div class="radio">
                            <input type="radio" required id="No" value="No" class="radio_input"/>
                            <label for="No" class="radio_label">No</label>
                        </div>
                        <div class="radio">
                            <input type="radio" required id="Yes" value="Yes" class="radio_input"/>
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
                    </div>
                    
                    <!--input label-->
                    <label for="keyContacts" class="user_label heading">
                        Key contacts
                    </label>
                    <div class="required">
                        <input type="Text" id="keyContacts" required class="user_input" />
                        <span class="dot"></span>
                    </div>
            </div>

        <!--right btn-->
            <button class="form_next_btn" v-if="showButton === 2" @click="toggleShowElement">                    
                Next
            </button>

        <!--section_3-->
            <div class="section" v-if="showElement === 3">
            
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

        <!----desktop---->

        <div class="desktop_only" v-else>
            <!--section_1-->
            <div class="section" >

            <!--Heading-->
            <div class="form_heading">
                Section 1
            </div>

            <!--Dropdown list-->
            <div class="required">
                <div class="user_select">
                    <div class="selected-value" @click="showOptions = !showOptions">
                        {{ selected }}         <span class="down-arrow">▼</span>
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
            </div>

            <!--right btn-->
            <button class="form_next_btn">                    
            Next
            </button>

            <!--section_2-->
            <div class="section">

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
                        <div class="user_label">Database Platform</div>
                        <span class="dot"></span>
                    </div>
                    <div class="radio">
                        <input type="radio" required id="relativity" value="Relativity" class="radio_input"/>
                        <label for="Relativity" class="radio_label">Relativity</label>
                    </div>
                    <div class="radio">
                        <input type="radio" required id="Disco" value="Disco" class="radio_input"/>
                        <label for="Disco" class="radio_label">Disco</label>
                    </div>
                    <div class="radio">
                        <input type="radio" required id="Accelerate" value="Accelerate" class="radio_input"/>
                        <label for="Accelerate" class="radio_label">Accelerate</label>
                    </div>
                    <div class="radio">
                        <input type="radio" required id="Other" value="Other" class="radio_input"/>
                        <label for="Other" class="radio_label">Other</label>
                    </div>
                </div>

                <!--radio group 2-->
                <div class="radio_wrapper">
                    <div class="required">
                        <div class="user_label">Scope</div>
                        <span class="dot"></span>
                    </div>
                    <div class="radio">
                        <input type="radio" required id="Standardreview" value="Standardreview" class="radio_input"/>
                        <label for="Standardreview" class="radio_label">Standard review</label>
                    </div>
                    <div class="radio">
                        <input type="radio" required id="Other" value="Other" class="radio_input"/>
                        <label for="Other" class="radio_label">Other</label>
                    </div>
                </div>

                <!--radio group 3-->
                <div class="radio_wrapper">
                    <div class="required">
                        <div class="user_label">Has foreign language?</div>
                        <span class="dot"></span>
                    </div>
                    <div class="radio">
                        <input type="radio" required id="No" value="No" class="radio_input"/>
                        <label for="No" class="radio_label">No</label>
                    </div>
                    <div class="radio">
                        <input type="radio" required id="Yes" value="Yes" class="radio_input"/>
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
                </div>
                
                <!--input label-->
                <label for="keyContacts" class="user_label heading">
                    Key contacts
                </label>
                <div class="required">
                    <input type="Text" id="keyContacts" required class="user_input" />
                    <span class="dot"></span>
                </div>
            </div>

            <!--right btn-->
            <button class="form_next_btn">                    
            Next
            </button>

            <!--section_3-->
            <div class="section">

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
                showElement: 1,
                showButton: 2,
                
            }
        },
        methods: {
            selectOption(option) {
                this.selected = option;
                this.showOptions = false;
            },
            toggleShowElement() {
                if (this.showElement === 1) {
                    this.showElement = 2;
                    this.showButton = 2;
                } else if (this.showElement === 2) {
                    this.showElement = 3;
                    this.showButton = 0;
                }
            }
        },
        computed: {
            isMobileView() {
            return window.innerWidth <= 800;
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
    .form_wrapper {
        max-width:350px;
        width:100%;
        display: flex;
        background-color: #8f8f8f29;
        flex-flow: column nowrap;
        border-radius: 25px;
        padding: 25px 30px;
    }

    //hidden elements
    .desktop_only {
        display: none;
    }

    //FORM SECTION
    .section {
        max-width: 330px;
        width: 100%;
        display:flex;
        flex-flow: column nowrap;
    }

    //BUTTON STYLE
    .form_submit_btn,
    .form_next_btn {
        
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
        margin-bottom: 20px;
        
        &:nth-of-type(2) {
            margin-top: 20px;
        }
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
        max-width: 285px;
        width:100%;
        display: flex;
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
            height: 6px;
            width: 6px;
            background-color: red;
            border-radius: 100%;
            margin-left: 2px;
        }
    }  

    //RADIO STYLES
    .radio{
        padding-top: 10px;
        padding-bottom: 5px;
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
    
    // MQ

    @media only screen and (min-width: 800px) {
        .form_wrapper {
            max-width:1300px;
            width:100%;
            background-color: #8f8f8f29;
            padding: 20px;
            border-radius: 25px;

            .desktop_only {
                display: flex;
                justify-content: space-around;
                .form_next_btn {
                    display: none;
                }
                .form_submit_btn {
                    align-self: flex-end;
                    margin-right: 29px;
                }

    
            }
        }
     
    }

    

</style>