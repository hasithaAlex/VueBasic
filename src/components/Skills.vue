<template>
  <div class="container">
    <div class="holder">
      <form @submit.prevent="addSkill">
        <input type="text" placeholder="Enter a skill you have.." v-model="skill">
        <input type="checkbox" id="checkbox" v-model="checked">
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
        checked: false,
        skills:[
          {skill:'Vue.js'},
          {skill:'Angular.js'},
        ],
      }
  },
  methods:{
    addSkill() {
      this.skills.push({skill: this.skill});
      this.skill = '';
      console.log(this.checked); 
    }
  }
}  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="./Skills.css" scoped></style>
