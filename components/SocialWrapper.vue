<template>
    <div class="social__wrapper">
        <SocialCard iconImage="soc-1.svg" />
        <SocialCard iconImage="soc-2.svg" />
        <SocialCard iconImage="soc-3.svg" />
        <SocialCard iconImage="soc-4.svg" />
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
