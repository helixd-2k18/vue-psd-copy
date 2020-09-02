<template>
<div class="intro">
    <div class="desc">
        <h1>lorem Ipsum Dolor sit amet</h1>
        <span>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamc
        </span>
        <div class="buttons">
            <div class="button dark">Buy now</div>
            <div class="button white">Try for free</div>
        </div>
    </div>
    <div></div>
    <div class="video">

    </div>
</div>
</template>

<script>
export default {
    name: 'NavBar',
    props: {
        msg: String
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style lang="scss" scoped>
@import "scss/library";

* {
    box-sizing: border-box;
}

.intro {
    padding-top: dpi(5);
    display: grid;
    grid-template-columns: dpi(20) 1fr dpi(20);
    color: white;

    &>.desc {
        display: flex;
        flex-direction: column;

        &>h1 {
            text-transform: uppercase;
            line-height: 1.2;
            font-size: dpi(2);
        }

        &>span {
            font-size: dpi(0.6);
            line-height: 2;
        }

        &>.buttons {
            display: flex;
            flex-direction: row;

            &>.button {
                @include button();
                margin-top: dpi(1);
                margin-right: dpi(1);
                border-radius: 5px;

                &.dark {
                    background-color: rgba(6, 30, 55, 1.0);
                    color: white;
                }

                &.white {
                    background-color: rgba(255, 255, 255, 1.0);
                    color: black;
                }
            }
        }
    }

    &>.video {
        width: 100%;
        height: calc(calc(dpi(20) / 16) * 9);
        background-color: rgb(240, 240, 240);
        border-radius: 2px;
    }
}
</style>
