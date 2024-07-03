<template>
    <div class="container_last">
        <CardLastNews
            imageName="1.jpeg"
            subtitle="Новая клиника в Стамбуле"
            date="27 июня 2024"
            text="Открываем новое отделение с инновационными методами лечения. Приходите и убедитесь сами!"
        />
        <CardLastNews
            imageName="2.jpeg"
            subtitle="Эксклюзивное Лечение в Анталии"
            date="25 июня 2024"
            text="Новые процедуры для наших клиентов в самом сердце курортного города. Бронируйте уже сегодня!"
        />
        <CardLastNews
            imageName="3.jpeg"
            subtitle="Измир: Оазис Здоровья"
            date="23 июня 2024"
            text="Открываем новый центр с уникальными методиками лечения. Приглашаем всех желающих на экскурсию!"
        />
        <CardLastNews
            imageName="4.jpeg"
            subtitle="Лучшие Процедуры в Турции"
            date="21 июня 2024"
            text="Наши клиники предлагают самые передовые методы лечения. Приходите и убедитесь сами в качестве обслуживания!"
        />
    </div>
</template>

<style lang="scss" scoped>
.container_last {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
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
