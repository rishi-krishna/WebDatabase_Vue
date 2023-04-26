<template>
    <div>
        <h2>{{ car.car_name }}</h2>
        <h2>{{ car.car_price }}</h2>
        <h2>{{ car.car_model }}</h2>
        <h2>{{ car.car_manufacture_date }}</h2>
        <h2>{{ car.car_reference_url }}</h2>
    </div>
</template>

<script>

export default{
    name: 'SingleCar',
    props:{
        car: Array
    }
}
</script>

<style scoped>
h2{
    margin: 2px;
}

div{
    background-color: #9effae;
    color: black;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
}

</style>