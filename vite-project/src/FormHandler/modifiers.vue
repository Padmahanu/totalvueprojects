<template>
    <div>
<h2> JOB FORM </h2>
 <form @submit.prevent="handleclick">
    <label for="name"> Name {{formvalues.name}}
        </label>
        <input type="text" id="name" v-model.trim.lazy="formvalues.name"/><br/>
        <label for="email"> Email
        </label>
        <input type="email" id="email" v-model="formvalues.email"/><br/>
        <label for="state"> State
        </label>
        <select name="state" id="state" v-model="formvalues.state">
            <option value="SelectCountery">SelectCountery</option>
                 <option value="India">India</option>
                      <option value="US">US</option>
                           <option value="UAS">UAS</option>

        </select><br/>
          <label for="skills"> Skill Set
        </label>
        <select name="skills" id="skills" multiple v-model="formvalues.skills">
            <option value="JAva">JAva</option>
                 <option value="C++">C++</option>
                      <option value="React">React</option>
                           <option value="VUE">VUE</option>

        </select><br/>
        
        <input type="checkbox" id="remote" name="remote" v-model="formvalues.uncheck" true-value="yes" false-value="no"/>
         <label for="remote"> Open to Remote work
        </label>
 <input type="number" id="age" name="age" v-model.number="formvalues.age" />
         <label for="age"> Age: 
        </label>

        <button>Submit</button>

</form>
    </div>
</template>

<script>
    export default {
        name:"App",
        data() {
            return {
                formvalues:{
              name:'',
              email:'',
              state:'',
              skills:[],
              uncheck:false,
              age:null
                }
            }
        },
        methods: {
            handleclick(){
                console.log("Form",this.formvalues)
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>