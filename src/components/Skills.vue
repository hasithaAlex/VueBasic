<template>
  <div class="hello">

    <div v-bind:class="{ alert: showAlert, 'another-class': showclass }"> alert</div>
    <div v-bind:class="{ alert: !showAlert, 'another-class': showclass}"> alert</div>

    <div v-bind:class="alertObject"> alert</div>

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
      }
  }
}  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="./Skills.css" scoped></style>
