<template>
<div class="features grid-4">
    <div class="feature n1">
        <div class="icon"><i class="icofont-business-man-alt-1"></i></div>
        <div class="text">
            12000+<br />
            Business
        </div>
    </div>
    <div class="feature n2">
        <div class="icon"><i class="icofont-download-alt"></i></div>
        <div class="text">
            60000+<br />
            Downloads
        </div>
    </div>
    <div class="feature n3">
        <div class="icon"><i class="icofont-compass-alt"></i></div>
        <div class="text">
            30000+<br />
            Free Installs
        </div>
    </div>
    <div class="feature n4">
        <div class="icon"><i class="icofont-download-alt"></i></div>
        <div class="text">
            40000+<br />
            Pro Users
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'Features',
    props: {
        msg: String
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style lang="scss" scoped>
@import "scss/library";

.features {
    .feature {
        text-align: center;
        color: white;
        height: dpi(6);
        font-weight: bold;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;

        .icon {
            padding: dpi(0.25);
            font-size: dpi(1.5);
        }

        .text {
            line-height: 1.2;
            padding: dpi(0.25);
            font-size: dpi(0.6);
            text-align: left;
        }

        &.n1 {
            background-color: #80d8ff;
        }

        &.n2 {
            background-color: #82b1ff;
        }

        &.n3 {
            background-color: #b388ff;
        }

        &.n4 {
            background-color: #ea80fc;
        }
    }
}

* {
    box-sizing: border-box;
}
</style>
