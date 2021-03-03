<template>
    <div class="value">
        <figure class="image-value">
            <slot name="image"></slot>
            <div class="circle"><p><slot name="number"></slot></p></div>
        </figure>
        <article>
            <h4><slot name="title"></slot></h4>
            <p><slot name="text"></slot></p>
        </article>
    </div>
</template>

<style lang="scss" scoped>
$yellow: #FCB72B;
$darkNavy: #495567;
$dimGrey: #939CAA;
    .value {
        width: 350px;
        height: 512px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        figure {
            width: 350px;
            height: 350px;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0;
            img {
                border-radius: 50%;
            }
            .circle {
                height: 96px;
                width: 96px;
                border-radius: 50%;
                background-color: $yellow;
                display: flex;
                justify-content: center;
                align-items: center;
                position: absolute;
                bottom: 0;
                p {
                    font-size: 24px;
                }
            }
        }
        article {
            width: 350px;
            height: 130px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            h4, p {
                margin: 0;
                text-align: center;
            }
            h4 {
                color: $darkNavy;
            }
            p {
                color: $dimGrey;
            }
        }
    }
</style>