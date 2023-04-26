<template>

  <!--Step 3 use the component-->
   <MyHeader CompanyTitle="Automobile Dictionary" Manager="Rishi Krishna Thodupunuri" />
   <CarBox :carDetails=carDetails />
</template>

<script>
// Step: 1 Import the components
import MyHeader from './components/MyHeader.vue';
import CarBox from './components/CarBox.vue';

export default {
  name: 'App',

  
  // Step 2: Register the components
  components: {
    MyHeader,
    CarBox
  },
  data(){
    return {
      carDetails: []
    } 
  },
  methods:{
    //promises
    async fetchcardetails(){
      const res = await fetch('https://rishi-thodupunuri.onrender.com/api');
      const data = await res.json();
      console.log(data);
      return data;
    }
  },
  async created(){
    this.carDetails = await this.fetchcardetails();
  }

}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;

}


</style>

