<template>
  <div class="hello">

    <div v-bind:class="{ alert: showAlert, 'another-class': showclass }"> class</div>
    <div v-bind:class="{ alert: !showAlert, 'another-class': showclass}"> class</div>

    <div v-bind:class="alertObject"> class </div>

    <div v-bind:style="{backgroundColor: bgGreen}"> style </div>


  </div>
</template>

<script> 
export default {
  name: 'Skills',
  data(){
      return {
        showAlert: true,
        showclass: true,
        alertObject: {
          alert: true,
          'another-class': true
        },
        bgGreen:'green'
      }
  }
}  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="./Skills.css" scoped></style>
