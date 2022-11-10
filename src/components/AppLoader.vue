<script>
export default {
    name: "AppLoader"
}

</script>

<template>
    <section class="ms_splash-screen">
        <div class="ms_loading">
        </div>
        <div class="ms_load-text">
            LOADING
        </div>
    </section>
</template>

<style lang="scss">
@use "../styles/partials/variables" as *;

.ms_splash-screen {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 300px;
    height: 300px;
}

.ms_loading {
    width: 300px;
    height: 300px;
    border-top: 5px solid $col-white;
    border-bottom: 5px solid $col-white;
    border-radius: 50%;

    animation-name: load-anim;
    animation-duration: 1s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
}

.ms_load-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 100px;
    height: 100px;
    line-height: 100px;
    text-align: center;
}

@keyframes load-anim {
    0% {
        border-radius: 30%;
        transform: rotate(0deg);
    }

    50% {
        border-radius: 50%;
    }

    100% {
        border-radius: 30%;
        transform: rotate(360deg);
    }
}
</style>