<script setup>
const props = defineProps({
    iconImage: {
        type: String,
        default: 'soc-1.svg',
    },
    link: {
        type: String,
        default: '/',
    },
})
</script>
<template>
    <nuxt-link :to="link">
        <div class="social">
        <img :src="'/social/' + iconImage" alt="icon" />
    </div>
    </nuxt-link>
 
</template>

<style lang="scss" scoped>
.social {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 72px;
    height: 72px;
    background-color: $primary;
    border-radius: 50%;
    padding: 20px;
    @media(min-width:1500px) {
        width: 100px;
        height: 100px;
        padding: 25px;
    }
    & img {
        width: 100%;
        height: 100%;
    }
  
}
</style>
