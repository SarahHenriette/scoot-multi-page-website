<template>
    <article class="question" :class="active">
        <header>
            <h4>{{ question }}</h4>
            <svg @click="displayReply" v-if="chevron" xmlns="http://www.w3.org/2000/svg" width="18" height="12"><path fill="none" stroke="#FCB72B" stroke-width="3" d="M1 1l8 8 8-8"/></svg>
            <svg @click="hideReply" v-else :class="active" xmlns="http://www.w3.org/2000/svg" width="18" height="12"><path fill="none" stroke="#FCB72B" stroke-width="3" d="M1 1l8 8 8-8"/></svg>
        </header>
        <main :class="active">
            <p>To download the Scoot app, you can search “Scoot” in both the App and Google Play stores. An even simpler way to do it would be to click the relevant link at the bottom of this page and you’ll be re-directed to the correct page.</p>
        </main>
    </article>

</template>
    
<script>
export default {
    props: ['question'],
    data () {
        return {
            chevron: true,
            active: ''
        }
    },
    methods: {
        displayReply(){
            this.active= 'active'
            this.chevron = false
        },
        hideReply(){
            this.active= ''
            this.chevron = true
        },

    }
}
</script>

<style lang="scss" scoped>
$snow: #F2F5F9;
$darkNavy: #495567;
$lightYellow: #FFF4DF;
    .question {
        width: 100%;
        height: 92px;
        background-color: $snow;
        margin-bottom: 16px;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        transition: height .1s linear;
        header {
            width: 650px;
            height: 28px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: auto;
            h4 {
                margin: 0;
                color: $darkNavy;
            }
            svg {
                cursor: pointer;
                padding: 20px;

            }
            svg.active {
                transform: rotate(180deg);
                cursor: pointer;
                padding: 20px;
            }
        }
        main {
            margin: 0 auto;
            display: none;
            transition: all .5s linear;
            p {
                width: 650px;
                height: 75px;
                margin: 0 auto 0 auto;
                color: $darkNavy;
            }
        }
        main.active {
            display: block;
        }

        &:hover {
            background-color: $lightYellow;
        }
    }

    .question.active {
        height: 191px;
        header {
            margin: 32px auto 24px auto;
        }
    }

@media screen and (max-width: 1200px) {
  .question {
      header {
          width: 617px;
      }
      main {
          p {
              width: 617px;
          }
      }
  }
}
@media screen and (max-width: 600px) {
    .question {
      header {
        width: 251px;
        height: 48px;
        h4 {
            font-size: 18px!important;
            line-height: 24px!important;
            width: 214px;
        }
      }
      main {
          p {
              width: 251px;
              height: 175px;
          }
      }
  }
  .question.active {
        height: 311px;
    }
}
</style>