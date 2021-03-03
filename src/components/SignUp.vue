<template>
    <section id="sign-up">
        <svg xmlns="http://www.w3.org/2000/svg" class="background-sign-up" width="1158" height="158"><g fill="none" fill-rule="evenodd" opacity=".1" transform="matrix(-1 0 0 1 1159 8)"><circle cx="173.5" cy="173.5" r="173.5" fill="#E5ECF4"/><circle cx="576.5" cy="173.5" r="173.5" stroke="#E5ECF4" stroke-width="15"/><circle cx="979.5" cy="173.5" r="173.5" stroke="#E5ECF4" stroke-width="15"/></g></svg>    
        <div class="contain-sign-up">
            <h2>Sign up and Scoot off today</h2>
            <div class="app-store-and-google-play">
                <img src="../../public/icons/app-store.svg" alt="">
                <img src="../../public/icons/google-play.svg" alt="">
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
  $darkNavy: #495567;
  $white: #FFF;
    #sign-up {
        width: 100%;
        height: 300px;
        background-color: $darkNavy;
        position: relative;
        display: flex;
        overflow: hidden;
        margin-top: 40px;
        .background-sign-up {
            position: absolute;
            bottom: 0;
            right: -163px;
        }
        .contain-sign-up {
            width: 1179px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: auto;
            h2 {
                color: $white;
                width: 484px;
                height: 96px;
                margin: 0;
            }
            .app-store-and-google-play {
                width: 359px;
                height: 56px;
                display: flex;
                justify-content: space-between;
            }
        }
    }

    @media screen and (max-width: 1110px) {
        #sign-up {
            flex-direction: column;
            .contain-sign-up {
                width: 487px;
                height: 176px;
                flex-direction: column;
                h2 {
                    width: 100%;
                    text-align: center;
                }
                .app-store-and-google-play {
                    width: 256px;
                    height: 40px;
                }
            }
        }
    }

      @media screen and (max-width: 700px) {
        #sign-up {
            .contain-sign-up {
                width: 311px;
                height: 185px;
                h2 {
                    font-size: 32px!important;
                    line-height: 32px!important;
                }
            }
        }
    }
</style>