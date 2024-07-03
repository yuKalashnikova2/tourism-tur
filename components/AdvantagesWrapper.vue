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
    @media(max-width: 992px) {
            grid-template-columns: repeat(2, 1fr);
            gap: 0.5rem;    
        }
        @media(max-width: 768px) {
            display: flex;
            flex-direction: column;
            // grid-template-columns: repeat(1, 1fr);
            gap: 1rem;
        }
}
</style>
