<template>
    <div class="single-car">
        <h2>{{ car.car_name }}</h2>
        <p class="car-info">Price: {{ car.car_price }}</p>
        <p class="car-info">Model: {{ car.car_model }}</p>
        <p class="car-info">Manufacture Date: {{ car.manufacture_date }}</p>
        <a :href="car.reference_url" target="_blank" class="car-link">Reference</a>

    </div>
</template>

<script>

export default {
    name: 'SingleCar',
    props: {
        car: Array
    }
}
</script>

<style scoped>
h2 {
    margin: 2px;
}

.single-car {
    background-color: #9effae;
    color: black;
    padding: 1em;
    text-align: center;
    width: 300px;
    margin: 10px;
}

.car-info {
    margin: 5px 0;
}

.car-link {
    display: block;
    margin-top: 10px;
    color: #0057ff;
    text-decoration: none;
}

.car-link:hover {
    text-decoration: underline;
}
</style>