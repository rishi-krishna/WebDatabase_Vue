<template>
    <div v-for="car of carDetails.carDetails" :key="car._id" >
       <SingleCar :car=car />
    </div>
</template>


<script>
import SingleCar from './SingleCar.vue';

export default {
    name: 'CarBox',
    props:{
        carDetails: Array
    },
    components:{
        SingleCar
    }
    
}
</script>
<style scoped>
div{
    background-color: blue;
}

</style>
