<template>
    <div class="container_last" id="lastnews">
        <CardLastNews imageName="1.jpg" />
        <CardLastNews imageName="2.jpg" />
        <CardLastNews imageName="3.jpg" />
        <CardLastNews imageName="4.jpg" />
    </div>
</template>

<style lang="scss" scoped>
.container_last {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 32px;
    align-items: stretch;
    margin-top: 3rem !important;
    @media (max-width: 1250px) {
        grid-template-columns: repeat(2, 1fr);
        gap: 1.5rem;
    }
    @media (max-width: 768px) {
        grid-template-columns: repeat(1, 1fr);
        gap: 1rem;
    }
}
</style>
