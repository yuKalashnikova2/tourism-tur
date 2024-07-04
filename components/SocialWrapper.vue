<template>
    <div class="social__wrapper">
        <SocialCard
            iconImage="soc-1.svg"
            link="https://instagram.com/zdorovekrasotaiturizm"
        />
        <SocialCard
            iconImage="soc-5.svg"
            link="https://vk.com/zdorovekrasotaiturizm"
        />
        <SocialCard
            iconImage="soc-6.svg"
            link="https://t.me/zdorovekrasotaiturizm"
        />
    </div>
</template>

<style lang="scss" scoped>
.social__wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 16px;
    margin-top: 3rem !important;
    @media (max-width: 768px) {
        flex-wrap: wrap;
    }
}
</style>
