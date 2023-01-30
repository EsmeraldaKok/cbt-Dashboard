<template>
    <div class="custom_select">
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
</template>

<script>
    export default {
        name: "CustomSelect",
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
    .custom_select {
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
    
</style>