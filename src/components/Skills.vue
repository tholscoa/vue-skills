<template>
  <div class="hello">
   <!-- {{ name }} Skills 
   
{{ btnState ? 'The button is active' : 'The button is disabled' }} -->
   <!-- <button v-on:click="changeName" v-bind:disable="btnState">Change Name</button> -->

   <div>
     <ul >
       <li v-for="(data, index) in skills" :key="index">{{index + ". "+data.skill}}</li>
       <!-- <li v-for="(data, index) in skills" :key="index">{{ data.skill }}</li> -->
     </ul>

     <p v-if="skills.length > 1">You have more than 1 skills</p>
     <p v-else>You  have less or equal to 1 one skills</p>
   </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data(){
    return{
      name: 'Isaac',
      btnState: true,
      skills: [
        {'skill': 'Frontend Dev' },
        {'skill': 'VueJS' },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
