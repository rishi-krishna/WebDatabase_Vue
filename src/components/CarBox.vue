<template>
    <div class="car-box">
        <div v-for="car of carDetails.CarDetails" :key="car._id" class="car-item">
            <SingleCar :car=car />
        </div>
    </div>
</template>


<script>
import SingleCar from './SingleCar.vue';

export default {
    name: 'CarBox',
    props: {
        carDetails: Array
    },
    components: {
        SingleCar
    }

}
</script>
<style scoped>
.car-box {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.car-item {
    margin: 10px;
}
</style>
