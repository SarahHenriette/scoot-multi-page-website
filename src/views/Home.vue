<template>
  <div class="home">
    <HeaderHome />
    <BreakPointsHome />
    <main>
     <div class="contain-article contain-telemetry">
        <Article class="article-telemetry">
        <template v-slot:title>Easy to use riding telemetry</template>
        <template v-slot:text>The Scoot app is available with riding telemetry. This means it can show you your average speed, how long you've been using the scooter, your traveling distance, and many more things all in an easy to use app.</template>
        <template v-slot:photo><img src="images/telemetry.jpg" alt="jeune femme tenant un telephone avec sa main droite"></template>
        <template v-slot:decoration><svg xmlns="http://www.w3.org/2000/svg" width="741" height="151"><g fill="none" fill-rule="evenodd" stroke="#FCB72B" stroke-linejoin="bevel" stroke-width="15"><path d="M740.969 8H182.854v99.369H6.591"/><path d="M44.64 145.64L6.214 107.214 44.64 68.787"/></g></svg></template>
        <template v-slot:button><Button text="Learn More" class="btn-article"/></template>
      </Article>
     </div>
    <div class="contain-article contain-near-you">
         <Article class="article-near-you">
          <template v-slot:title>Coming to a city near you</template>
          <template v-slot:text>Scoot is available in 4 major cities so far. We’re expanding rapidly, so be sure to let us know if you want to see us in your hometown. We’re aiming to let our scooters loose on 23 cities over the coming year.</template>
          <template v-slot:photo><img src="images/near-you.jpg" alt="vue sur une route entourer de batiments"></template>
          <template v-slot:decoration><svg xmlns="http://www.w3.org/2000/svg" class="arrow-2" width="452" height="151"><g fill="none" fill-rule="evenodd" stroke="#FCB72B" stroke-linejoin="bevel" stroke-width="15"><path d="M407.952 145.444l38.426-38.426-38.426-38.426"/><path d="M0 8h270.115v99.369h176.263"/></g></svg></template>
          <template v-slot:button><Button text="Learn More" class="btn-article"/></template>
        </Article>
    </div>
    <div class="contain-article contain-payments">
        <Article class="article-payments">
          <template v-slot:title>Zero hassle payments</template>
          <template v-slot:text>Our payment is as easy as one two three. We accept most credit cards and debit cards. You can also link your PayPal account inside the app. Need to pay later? No worries! You can defer payment for up to a month.</template>
          <template v-slot:photo><img src="images/payments.jpg" alt="personne sortant de l'argent de son portefeuille"></template>
          <template v-slot:decoration><svg xmlns="http://www.w3.org/2000/svg" class="arrow-3" width="741" height="151"><g fill="none" fill-rule="evenodd" stroke="#FCB72B" stroke-linejoin="bevel" stroke-width="15"><path d="M740.969 8H182.854v99.369H6.591"/><path d="M44.64 145.64L6.214 107.214 44.64 68.787"/></g></svg></template>
          <template v-slot:button><Button text="Learn More" class="btn-article"/></template>
      </Article>
    </div>

    </main>
  </div>
</template>

<script>
import HeaderHome from './../components/HeaderHome'
import BreakPointsHome from './../components/BreakPointsHome'
import Article from './../components/Article'
import Button from './../components/Button'

export default {
  name: 'Home',

  components: {
    Button,
    Article,
    HeaderHome,
    BreakPointsHome,
    
  }
}
</script>

<style lang="scss" scoped>
$white: #FFF;
$lightGrey: #E5ECF4;


  main {
    overflow: hidden;
    width: 100%;
    margin: auto;
    .contain-article {
      width: 100%;
      margin-bottom: 160px;
      .article-telemetry { 
        width: 1619px;
         svg{
          position: absolute;
          left: 0;
          bottom: 0;
        }
      }
      .article-near-you {
        width: 1660px;
        svg {
          position: absolute;
          top: 0;
          right: 260px;
        }
      }
      .article-payments {
        width: 1655px;
         svg {
          position: absolute;
          top: 85px;
          left: 255px;
        }
      }
    }

  @media screen and (max-width: 1435px) {
    main {
      width: 100%;
     .contain-article {
       .article-telemetry {
          svg {
            left: -5%;
          }
      }

      .article-near-you {
          svg {
            right: 0;
            left: 0;
          }
        }
     }
    }
  }

    @media screen and (max-width: 1245px) {
      .contain-article {
       .article-telemetry {
          svg {
            left: -5%;
          }
      }

      .article-near-you {
          svg {
            right: 0;
            left: 0;
          }
        }
     }
     
  }

    @media screen and (max-width: 415px) {
      .contain-article {
       .article-telemetry {
          svg {
            left: 0;
          }
      }

      .article-near-you {
          svg {
            right: 8%;
            left: auto;
          }
        }
     }
    }
  }





</style>
