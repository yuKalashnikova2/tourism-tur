<script setup>
import { ref } from 'vue'
const cities = ref([
    {
        cityName: 'Стамбул',
        image: 'city-1.jpeg',
        info: 'История и современность в одном месте',
    },
    {
        cityName: 'Анталья',
        image: 'city-2.jpeg',
        info: 'Солнце, море и красота ждут вас',
    },
    {
        cityName: 'Измир',
        image: 'city-3.jpeg',
        info: 'Уютный город на берегу Эгейского моря',
    },
])
</script>
<template>
    <div class="cities">
        <CardCities
            v-for="city in cities"
            :key="city.cityName"
            :city-name="city.cityName"
            :image="city.image"
            :info="city.info"
        />
    </div>
</template>

<style lang="scss" scoped>
.cities {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 32px;
    align-items: stretch;
    margin-top: 3rem !important;
}
</style>
