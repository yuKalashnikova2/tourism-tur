<template>
    <div class="contacts__wrapper">
        <ContactCard title="Телефон" descry="+7 925 499 45 61" />
        <ContactCard title="Email" descry="eyupahmetuygun@mail.ru" />
        <ContactCard title="Адрес" descry="Москва, Улица А, дом 3, Россия" />
        <ContactCard title="Часы работы" descry="Пн-Пт: 9:00-18:00" />
    </div>
</template>

<style lang="scss" scoped>
.contacts__wrapper {
    margin-top: 3rem !important;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: auto;
    gap: 2rem;
    @media (max-width: 768px) {
        grid-template-columns: repeat(1, 1fr);
        gap: 1rem;
    }
}
</style>
