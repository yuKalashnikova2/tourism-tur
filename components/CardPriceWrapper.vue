<template>
    <div class="price">
        <CardPrice packageName="Стандарт" :price="999" text="Операция + отдых + гарантированный результат. Все включено!" />
        <CardPrice packageName="Премиум" :price="1999" text="VIP обслуживание, персональный подход, роскошное проживание. Лучшее из лучшего!" />
        <CardPrice packageName="Эксклюзив" :price="2999" text="Индивидуальный маршрут, эксклюзивные процедуры, 24/7 поддержка. Для истинных ценителей!" />
        <CardPrice packageName="VIP" :price="4999" text="Процедуры на высшем уровне, личный врач, роскошное лечение. Для тех, кто заслуживает только лучшее!" />
    </div>
</template>

<style lang="scss" scoped>
    .price {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 32px;
        align-items: stretch;
        margin-top: 3rem !important;

    }
</style>