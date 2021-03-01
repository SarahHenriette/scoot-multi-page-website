<template>
    <div class="break-point">
        <div class="contain-image">
            <img :src= image alt="">
        </div>
        <div class="text-break-point">
            <h4>{{ title }}</h4>
            <p>{{ text }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['image', 'title', 'text']
    }
</script>

<style lang="scss" scoped>
$darkNavy: #495567;
$dimGrey: #939CAA;
    .break-point {
        width: 350px;
        height: 291px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: flex-start;
        margin-left: 30px;
        
        h4, p{
            margin: 0;
        }
        h4 {
            color: $darkNavy;
        }
        p {
            color: $dimGrey;
        }
    }

    @media screen and (max-width: 1300px) {
        .break-point {
            width: 100%;
            flex-direction: row;
            margin-left: 0;
            .text-break-point {
                width: 398px;
                height: 130px;
                display: flex;
                flex-direction: column;
                justify-content: space-between;
            }
        }
    }

      @media screen and (max-width: 700px) {
        .break-point {
            width: 311px;
            height: 232px;
            flex-direction: column;
            margin-left: 0;
            .contain-image {
                margin: 0 auto;
                height: 56px;
                width: 56px;
                img {
                    width: 100%;
                    height: auto;
                }
            }
            .text-break-point {
                width: 311px;
                height: 152px;
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                align-items: center;
                p {
                    text-align: center;
                }
            }
        }
    }
</style>