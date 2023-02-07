<template>
                    <div>
                                        <pre>
                                        {{ JSON.stringify(formValues, null, 2) }}
                                        </pre>
                    </div>
                    <form @submit="submitForm">
                                        <div>
                                                            <label for="name">Name: </label><br/>
                                                            <input type="text" id="name" v-model="formValues.name">
                                        </div>

                                        <div>
                                                            <label for="profile">Profile Summary:</label><br/>
                                                            <textarea id="profile" v-model="formValues.profileSummary"/>
                                        </div>

                                        <div>
                                                            <label for="country">Country:</label><br/>
                                                            <select id="country" v-model="formValues.country">
                                                                                <option value="">Select a country</option>
                                                                                <option value="india">India</option>
                                                                                <option value="vietnam">Vietnam</option>
                                                                                <option value="singapore">Singapore</option>
                                                            </select>
                                        </div>

                                         <div>
                                                            <label for="job-location">Job Location:</label><br/>
                                                            <select id="job-location" multiple v-model="formValues.jobLocation">
                                                                                <option value="india">India</option>
                                                                                <option value="vietnam">Vietnam</option>
                                                                                <option value="singapore">Singapore</option>
                                                            </select>
                                        </div>
                                        <div>
                                                            <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork" true-value="yes"/>
                                                            <label for="remoteWork">Open to remote work?</label>
                                        </div>

                                        <label for="Skill set">Skill Set</label><br/>
                                        <input type="checkbox" id="html" value="html" v-model="formValues.skillSet"/>
                                        <label for="html">HTML</label>
                                        <input type="checkbox" id="css" value="css" v-model="formValues.skillSet"/>
                                        <label for="css">CSS</label>
                                        <input type="checkbox" id="js" value="js" v-model="formValues.skillSet"/>
                                        <label for="js">js</label>
                                        <br/>

                                        <label>Years of Experience</label><br/>

                                        <input type="radio" id= "0-2" value="0-2" v-model="formValues.yearOfExperience"/>
                                        <label for="0-2">0-2</label>

                                        <input type="radio" id= "3-5" value="3-5" v-model="formValues.yearOfExperience"/>
                                        <label for="3-5">3-5</label>

                                        <input type="radio" id= "6-10" value="6-10" v-model="formValues.yearOfExperience"/>
                                        <label for="6-10">6-10</label>

                                        <div>
                                                            <button class="btn">Submit</button>
                                        </div>
                    </form>
                   
</template>

<script>
                    export default {
                    name: 'Form-Handling',
                    data() {
                                        return {
                                                            formValues: {
                                                            name: '',
                                                                                profileSummary: '',
                                                                                jobLocation: [],
                                                                                country: '',
                                                                                remoteWork: 'no',
                                                                                skillSet: [],
                                                                                yearOfExperience:'',
                                                            
                                                            },                                    
                                        }
                    },
                    methods: {
                                        submitForm(event) {
                                                            event.preventDefault()
                                        console.log('Form values' , this.formValues)
                                }                            
                    }
                                        
                    }
</script>

<style scoped>


</style>