<template>
    <div class="contacts__wrapper" id="contacts">
        <ContactCard title="Телефон" descry="+7 925 499 45 61" />
        <ContactCard title="Email" descry="eyupahmetuygun@mail.ru" />
        <ContactCard title="WhatsApp" descry="+7 925 499 45 61" />
        <ContactCard title="Часы работы" descry="Каждый день с 9:00 до 18:00" />
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
