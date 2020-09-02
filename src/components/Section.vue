<template>
<div class="s-block">
    <div class="padding-center grid-1 main">
        <h1>Easy & Useful</h1>
        <h3>Project Management Tool</h3>
        <span>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud
        </span>
    </div>

    <div class="padding-normal grid-3">
        <div>
            <div><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="68px" height="70px">
                    <text kerning="auto" font-family="Myriad Pro" fill="rgb(0, 0, 0)" font-size="80px" x="0px" y="70.0630000000001px">
                        <tspan font-size="80px" font-family="icofont" fill="#B388FF">&#60036;</tspan>
                    </text>
                </svg></div>
            <h3>Title Goes Here</h3><span>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</span>
        </div>
        <div>
            <div><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="58px" height="80px">
                    <text kerning="auto" font-family="Myriad Pro" fill="rgb(0, 0, 0)" font-size="80px" x="0px" y="80.0630000000001px">
                        <tspan font-size="80px" font-family="icofont" fill="#80D8FF">&#61070;</tspan>
                    </text>
                </svg></div>
            <h3>Title Goes Here</h3><span>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</span>
        </div>
        <div>
            <div><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="68px" height="71px">
                    <text kerning="auto" font-family="Myriad Pro" fill="rgb(0, 0, 0)" font-size="80px" x="0px" y="71.0630000000001px">
                        <tspan font-size="80px" font-family="icofont" fill="#EA80FC">&#60411;</tspan>
                    </text>
                </svg></div>
            <h3>Title Goes Here</h3><span>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</span>
        </div>
    </div>

    <div class="padding-center grid-1">
        <div>
            <div class="button">Get Started</div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'Section',
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
    line-height: 1.6;
}

.s-block {
    width: 100%;
    height: dpi(30);
    text-align: center;
    margin: 0 auto;

    &>* {
        text-align: center;

        &>* {
            margin: 0 auto;
        }
    }

    .grid-3 {
        color: rgb(120, 144, 156);

        &>div {
            padding: dpi(2);
        }
    }

    .grid-1 {
        &.main {
            padding-top: dpi(3);

            h3,
            span {
                color: rgb(176, 190, 197);
            }
        }
    }

    .button {
        @include button();
        background-color: rgb(29, 233, 182);
        color: white;
        font-weight: bold;
        margin: 0 auto;
    }
}
</style>
