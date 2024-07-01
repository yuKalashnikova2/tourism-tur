<template>
    <div class="video">
        <iframe
            width="1000"
            height="615"
            src="https://www.youtube.com/embed/NN1l3MyhcXY?autoplay=1"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
        ></iframe>
    </div>
</template>

<style lang="scss" scoped>
.video {
    margin-top: 3rem !important;
    border-radius: 12px;
    overflow: hidden;
    position: relative;
    padding-bottom: 20%;
    height: 615px;
    & iframe {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;

        border-radius: 12px;
    }
}
</style>
