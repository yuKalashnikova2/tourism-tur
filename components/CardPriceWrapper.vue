<template>
    <div class="price" id="price">
        <CardPrice packageName="Лечение Грыжи без Операции" :price="999" text="Лечение с высокой технологией от грыжи и сильной боли без операции
" />
        <CardPrice packageName="Пересадка Волос
" :price="1999" text="Самые лучшие методы Сапфир FUI и DHI
" />
        <CardPrice packageName="Эстетика
" :price="2999" text="Медицинская эстетика, пластическая хирургия, липосакция и тд.
" />
        <CardPrice packageName="Стоматология
" :price="4999" text="Импланты, коронки, протезирование и отбеливание" />
    </div>
</template>

<style lang="scss" scoped>
    .price {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 32px;
        align-items: stretch;
        margin-top: 3rem !important;
     
        @media(max-width: 1200px) {
            grid-template-columns: repeat(2, 1fr);
            gap: 0.5rem;    
        }
        @media(max-width: 768px) {
            grid-template-columns: repeat(1, 1fr);
            gap: 1rem;
        }
    }
</style>