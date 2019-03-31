<template>
  <div class="container">
    <div class="holder">
      <form @submit.prevent="addSkill">
        <input type="text" placeholder="Enter a skill you have.." v-model="skill" v-validate="'min:5'" name="skill">
        <transition name="alert-in">
          <p class="alert" v-if="errors.has('skill')">{{errors.first('skill')}}</p>
        </transition>
        <ul>
          <li v-for="(data, index) in skills" :key='index'>{{data.skill}}</li>
        </ul>
        <p>These are the skills that you possess.</p>
      </form>
    </div>
  </div>
</template>


<script> 
export default {
  name: 'Skills',
  data(){
      return {
        skill:'',
        skills:[
          {skill:'Vue.js'},
          {skill:'Angular.js'},
        ],
      }
  },
  methods:{
    addSkill() {
      this.$validator.validateAll().then((result)=>{
        if(result){
          this.skills.push({skill: this.skill});
          this.skill = '';
        }
      })
    }
  }
}  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="./Skills.css" scoped></style>
