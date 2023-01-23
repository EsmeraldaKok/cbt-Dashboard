<template>
    <div class="container">

        <!--User header wrapper-->
        <div class="header_wrapper">

            <!-- back button-->
            <button class="back_btn">
                <svg id="Group_1253" data-name="Group 1253" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="28" height="28" viewBox="0 0 28 28">
                    <defs>
                        <clipPath id="clip-path">
                        <rect id="Rectangle_697" data-name="Rectangle 697" width="28" height="28" fill="#1d1e26"/>
                        </clipPath>
                    </defs>
                    <g id="Group_1252" data-name="Group 1252" clip-path="url(#clip-path)">
                        <path id="Path_2002" data-name="Path 2002" d="M14,28A14,14,0,1,0,0,14,14,14,0,0,0,14,28M8.96,12.99,15.2,6.75a1.35,1.35,0,0,1,.94-.39,1.315,1.315,0,0,1,.93,2.25L11.68,14l5.39,5.39a1.315,1.315,0,0,1-.93,2.25,1.292,1.292,0,0,1-.94-.39L8.96,15.01a1.424,1.424,0,0,1,0-2.02" fill="#1d1e26"/>
                    </g>
                </svg>
            </button>
            
            <!--Client-->
            <h4 class="client_heading">{{ companyName }}</h4>
        </div>
        <!--User info wrapper-->
        <div class="user_wrapper" v-for="(item, index) in items" :key="index">
                <!--Fullnames-->
                <div class="user_info">
                    <h4 class="user_info_heading">NAME</h4>
                    <span class="user_info_text">{{ item.name }}, {{ item.surname }}</span>
                </div>
                <!--Surname-->
                <div class="user_info">
                    <h4 class="user_info_heading">SURNAME</h4>
                    <span class="user_info_text">{{ item.surname }}</span>
                </div>
                
                <!--Email-->
                <div class="user_info">
                    <h4 class="user_info_heading">EMAIL</h4>
                    <span class="user_info_text">{{ item.email }}</span>
                </div>

                <!--Date created-->
                <div class="user_info">
                    <h4 class="user_info_heading">CREATED</h4>
                    <span class="user_info_text">{{ item.date_created }}</span>
                </div>

                <!--Notes-->
                <div class="user_info">
                    <h4 class="user_info_heading">NOTES</h4>
                    <span class="user_info_text">{{ item.notes }}</span>
                </div>
            
        </div>

        <!--User button wrapper-->
        <div class="button_wrapper">
            <div class="btn">
                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="45" height="45" viewBox="0 0 45 45">
                    <path 
                        id="Path_2001" 
                        data-name="Path 2001" 
                        d="M31.4,15.31a.426.426,0,0,0-.3-.14H13.622a.426.426,0,0,0-.3.14.371.371,0,0,0-.08.312l3.37,17.089a.389.389,0,0,0,.383.312H27.723a.389.389,0,0,0,.383-.312l3.37-17.089a.371.371,0,0,0-.08-.312M27.2,27.327a.8.8,0,0,1-1.15,1.124L22.357,24.83l-3.689,3.621a.8.8,0,0,1-1.15-1.124l3.7-3.605-3.7-3.605a.788.788,0,0,1,0-1.108.823.823,0,0,1,1.15,0l3.689,3.605,3.689-3.605a.823.823,0,0,1,1.15,0,.788.788,0,0,1,0,1.108l-3.7,3.605ZM31.4,15.31a.426.426,0,0,0-.3-.14H13.622a.426.426,0,0,0-.3.14.371.371,0,0,0-.08.312l3.37,17.089a.389.389,0,0,0,.383.312H27.723a.389.389,0,0,0,.383-.312l3.37-17.089a.371.371,0,0,0-.08-.312M27.2,27.327a.8.8,0,0,1-1.15,1.124L22.357,24.83l-3.689,3.621a.8.8,0,0,1-1.15-1.124l3.7-3.605-3.7-3.605a.788.788,0,0,1,0-1.108.823.823,0,0,1,1.15,0l3.689,3.605,3.689-3.605a.823.823,0,0,1,1.15,0,.788.788,0,0,1,0,1.108l-3.7,3.605ZM22.357,0A22.1,22.1,0,0,0,0,21.849,22.112,22.112,0,0,0,22.357,43.7,22.112,22.112,0,0,0,44.715,21.849,22.1,22.1,0,0,0,22.357,0M20.9,9.1h2.906a2.783,2.783,0,0,1,2.811,2.747.807.807,0,0,1-1.613,0,1.193,1.193,0,0,0-1.2-1.17H20.9a1.193,1.193,0,0,0-1.2,1.17.807.807,0,0,1-1.613,0A2.783,2.783,0,0,1,20.9,9.1m12.153,6.82-3.37,17.089A2,2,0,0,1,27.723,34.6H16.992a2,2,0,0,1-1.964-1.592l-3.37-17.089a1.967,1.967,0,0,1,1.964-2.325H31.093a1.967,1.967,0,0,1,1.964,2.325m-1.964-.749H13.622a.426.426,0,0,0-.3.14.371.371,0,0,0-.08.312l3.37,17.089a.389.389,0,0,0,.383.312H27.723a.389.389,0,0,0,.383-.312l3.37-17.089a.371.371,0,0,0-.08-.312.426.426,0,0,0-.3-.14M27.2,27.327a.8.8,0,0,1-1.15,1.124L22.357,24.83l-3.689,3.621a.8.8,0,0,1-1.15-1.124l3.7-3.605-3.7-3.605a.788.788,0,0,1,0-1.108.823.823,0,0,1,1.15,0l3.689,3.605,3.689-3.605a.823.823,0,0,1,1.15,0,.788.788,0,0,1,0,1.108l-3.7,3.605Z" 
                        transform="translate(-0.114 0.446)" 
                        fill="#f52f57"/>
                </svg>
            </div>
            <div class="btn">
                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="45" height="45" viewBox="0 0 45 45">
                    <path id="Path_2000" 
                        data-name="Path 2000"
                        d="M22.441,0A22.184,22.184,0,0,0,0,21.931,22.194,22.194,0,0,0,22.441,43.861,22.194,22.194,0,0,0,44.881,21.931,22.184,22.184,0,0,0,22.441,0M14.346,31.768a.951.951,0,0,1-.289.2L11.012,33.4a.224.224,0,0,1-.3-.3l1.443-2.961a1.467,1.467,0,0,1,.224-.3l16.4-16.025,1.972,1.942Zm19.539-19.08-1.523,1.488L30.375,12.25l1.539-1.5a1.092,1.092,0,0,1,1.539,0l.433.423a1.08,1.08,0,0,1,0,1.519" 
                        transform="translate(-0.458 0)" 
                        fill="#00c2d6" />
                </svg>

            </div>
        </div>

    </div>
</template>

<script>
    export default {
    name: 'UserInfo',
    data() {
        return {
            "items": items,
            companyName: "KFC",
        }
    }
}
//fake data
let items = [
    {
        "name": "Harland",

        "surname": "Sander",

        "email": "email@email.com",

        "date_created": "2022/01/17",

        "notes": "some note"
    }
]

</script>
<style lang="scss" scoped>

    /*google font */
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,300;0,400,0,700;0,900;1,500&display=swap');

    /* general  styles*/
    *, 
    *::after, 
    *::before {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'monserrat', sans-serif;
    }
    .container {
        max-width: 430px;
        width:100%;
        background-color: white;
        padding:12px;
        display: flex;
        flex-flow: column nowrap;
        align-items: flex-start;
        
        .header_wrapper {
            align-self: flex-start;
            display: flex;
            flex-flow: row nowrap;
            justify-content: flex-start;
            align-items: center;
            padding: 20px 15px;
            
            .back_btn {
                cursor: pointer;
                background-color: transparent;
                outline: none;
                border: none;
                
            }

            .client_heading {
                font-size: 24px;
                padding-left: 15px;
            }
        }
        .user_wrapper{
            align-self: start;
            display: flex;
            flex-flow: column nowrap;
            justify-content: space-between;
            align-items: flex-start;
            padding: 20px 15px;

            .user_info  {
                margin-bottom: 20px;

                &_heading {
                    font-size: 12px;
                    font-weight: 800;
                    color: black;
                    line-height: 15px;
                }
                &_text {
                    font-size: 16px;
                    font-weight: 300;
                    color: black;
                    line-height: 19px;
                }
            }
        }
        .button_wrapper {
            align-self: center;
            justify-self: flex-end;
            max-width: 430px;
            width: 100%;
            display: flex;
            flex-wrap: nowrap;
            justify-content: space-evenly;
            align-items: center;


            .btn {
                padding: 10px 15px;
            }
        }
    }
</style>