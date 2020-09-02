<template>
<div class="services">
    <div class="title padding-center">
        <h1>Services</h1>
        <span>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna</span>
    </div>
    <div class="cards padding-center-25">
        <div class="card open">
            <div class="head" @click="open">
                <div class="icon"><i class="icofont-chart-histogram"></i></div>
                <div class="text">Statistics</div>
                <div class="press"><i class="icofont-ui-check"></i></div>
            </div>
            <div class="body">
                <div class="img">
                    <img src="img/img.png" alt="" />
                </div>
                <div class="content">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
                </div>
            </div>
        </div>
        <div class="card">
            <div class="head" @click="open">
                <div class="icon"><i class="icofont-inbox"></i></div>
                <div class="text">Inbox</div>
                <div class="press"><i class="icofont-ui-check"></i></div>
            </div>
            <div class="body"></div>
        </div>
        <div class="card">
            <div class="head" @click="open">
                <div class="icon"><i class="icofont-team"></i></div>
                <div class="text">Team</div>
                <div class="press"><i class="icofont-ui-check"></i></div>
            </div>
            <div class="body"></div>
        </div>
        <div class="card">
            <div class="head" @click="open">
                <div class="icon"><i class="icofont-settings-alt"></i></div>
                <div class="text">Settings</div>
                <div class="press"><i class="icofont-ui-check"></i></div>
            </div>
            <div class="body"></div>
        </div>
        <div class="card">
            <div class="head" @click="open">
                <div class="icon"><i class="icofont-rss-feed"></i></div>
                <div class="text">Feed</div>
                <div class="press"><i class="icofont-ui-check"></i></div>
            </div>
            <div class="body"></div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'Services',
    props: {
        msg: String
    },
    methods: {
        open: function (e) {
            let head = e.target,
                card = head.parentNode.parentNode;
            let elements = document.querySelectorAll(".services .cards .card");
            for (let i = 0; i < elements.length; i++) {
                let element = elements[i];
                if (element == card) {
                    element.classList.toggle("open");
                } else {
                    element.classList.remove("open");
                }
            }
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style lang="scss" scoped>
@import "scss/library";

.services {
    height: dpi(35);

    .title {
        padding-top: dpi(1);
        height: dpi(8);

        &>span {
            color: #b0bec5;
        }
    }

    .cards {
        .card {
            transition: all .5s;
            font-size: dpi(0.6);
            width: calc(100% - dpi(0.5));
            margin-top: dpi(0.6);
            height: dpi(2.0);
            padding: dpi(1);
            padding-top: dpi(0.5);
            overflow: hidden;
            box-shadow: 1px 1px 5px rgba(0, 0, 0, 0.2);
            border-radius: 4px;

            .head {
                color: #061e37;
                cursor: pointer;
                user-select: none;

                padding-top: dpi(0.1);
                text-align: left;
                height: dpi(1.5);
                font-weight: bold;
                display: grid;
                grid-template-columns: dpi(0.5) 1fr dpi(0.5);

                .text {
                    padding-left: dpi(0.5);
                    padding-right: dpi(0.5);
                }
            }

            .body {
                color: #061e37;
                text-align: left;
                margin-top: dpi(0.0);
                display: flex;
                flex-direction: row;

                .content {
                    padding-left: dpi(1);
                }

                .img {}
            }
        }

        .open {
            box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.2);
            height: dpi(10);
        }
    }

}

* {
    box-sizing: border-box;
}
</style>
