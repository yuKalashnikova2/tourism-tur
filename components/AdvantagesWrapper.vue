<template>
    <div class="advantages">
        <AdvantagesCard quantity="1000" text="Счастливых пациентов" />
        <AdvantagesCard quantity="500" text="Успешных операций" />
        <AdvantagesCard quantity="24/7" text="Поддержка и гарантия" />
    </div>
</template>

<style lang="scss" scoped>
.advantages {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 32px;
}
</style>
