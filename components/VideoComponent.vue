<template>
    <div class="video">
        <video
            width="500"
            height="615"
            controls
            autoplay
            muted
            playsinline
        >
        <source src="/short.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
    </div>
</template>

<style lang="scss" scoped>
.video {
    margin-top: 3rem !important;
    border-radius: 12px;
    overflow: hidden;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
