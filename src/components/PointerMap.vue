<template>
    <div class="pointer">
        <div class="rectangle"><p>{{ city }}</p></div>
        <div class="triangle"></div>
    </div>
</template>

<script>
export default {
    props: ['city']
}
</script>

<style lang="scss" scoped>
  $yellow: #FCB72B;
  $darkNavy: #495567;

.pointer {
    width: 189px;
    height: 88px;
    position: absolute;
    display: flex;
    justify-content: center;

    .rectangle {
        width: 100%;
        height: 72px;
        background-color: $yellow;
        display: flex;
        justify-content: center;
        align-items: center;
        p {
            font-size: 24px!important;
            color: $darkNavy;
        }
    }
    .triangle {
        width: 0;
        height: 0;
        border-left: 16px solid transparent;
        border-right: 16px solid transparent;
        border-top: 18px solid $yellow;
        position: absolute;
        bottom: 0;
        
    }
}

@media screen and (max-width: 1200px)  {
    .pointer {
        width: 120px;
        height: 40px;
        .rectangle {
            height: 32px;
             p {
                font-size: 13px!important;
            }
        }
    }
}

@media screen and (max-width: 600px)  {
    .pointer {
        width: 16px;
        height: 16px;
        .rectangle {
            height: 16px;
            width: 16px;
            border-radius: 50%;
            p {
                display: none;
            }
        }
        .triangle {
            display: none;
        }
    }
}
</style>