<template>
  <div class="container">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in skills" :key='index'>{{data.skill}}</li>
      </ul>
      <p>These are the skills that you possess.</p>
    </div>
  </div>
</template>


<script> 
export default {
  name: 'Skills',
  data(){
      return {
        skills:[
          {skill:'Vue.js'},
          {skill:'Angular.js'},
        ]
      }
  }
}  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="./Skills.css" scoped></style>
