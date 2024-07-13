<script setup>
import { ref } from 'vue'
const cities = ref([
{
        cityName: 'Стамбул',
        image: 'city-3.jpg',
        info: 'История и современность в одном месте',
    },


    {
        cityName: 'Анталья',
        image: 'city-1.jpg',
        info: 'Солнце, море и красота ждут вас',
    },
    {
        cityName: 'Измир',
        image: 'city-2.jpg',
        info: 'Культурная столица на берегу Эгейского моря',
    },
])
</script>
<template>
    <div class="cities" >
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
    @media(max-width: 992px) {
            grid-template-columns: repeat(2, 1fr);
            gap: 0.5rem;    
        }
        @media(max-width: 768px) {
            grid-template-columns: repeat(1, 1fr);
            gap: 1rem;
        }
}
</style>
