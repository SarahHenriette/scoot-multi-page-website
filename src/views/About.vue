<template>
  <div class="about">
    <Header text="About" class="header-about"/>
    <main>
        <div class="contain-article contain-digital-era">
        <Article textButton="test" class="article-digital-era">
          <template v-slot:title>Mobility for the digital era</template>
          <template v-slot:text>Getting around should be simple (and even fun!) for everyone. We embrace technology to provide low cost, smart access to scooters at your fingertips.</template>
          <template v-slot:photo><img src="images/digital-era.jpg" alt="jeune femme regardant son telephone"></template>
          <template v-slot:decoration><svg xmlns="http://www.w3.org/2000/svg" width="741" height="151"><g fill="none" fill-rule="evenodd" stroke="#FCB72B" stroke-linejoin="bevel" stroke-width="15"><path d="M740.969 143.368H182.854V43.999H6.591"/><path d="M44.64 82.64L6.214 44.214 44.64 5.787"/></g></svg></template>
        </Article>
      </div>
      <div class="contain-article contain-better-living">
        <Article class="article-better-living">
          <template v-slot:title>Better urban living</template>
          <template v-slot:text>We’re helping connect cities and bring people closer together. Our scooters are also fully-electric and we offset the minimal carbon footprint for each ride.</template>
          <template v-slot:photo><img src="images/better-living.jpg" alt="vue sur un bus jaune"></template>
          <template v-slot:decoration><svg xmlns="http://www.w3.org/2000/svg" class="arrow-2" width="452" height="151"><g fill="none" fill-rule="evenodd" stroke="#FCB72B" stroke-linejoin="bevel" stroke-width="15"><path d="M407.952 145.444l38.426-38.426-38.426-38.426"/><path d="M0 8h270.115v99.369h176.263"/></g></svg></template>
        </Article>
      </div>

      <Values title="Our values" class="our-values"/>

      <section class="faq">
        <h2>FAQs</h2>
        <Faq>
           <template v-slot:title>How it works</template>
           <template v-slot:questions>
             <Question question= "How do I download the app?"/>
             <Question question= "Can I find a nearby Scoots?"/>
             <Question question= "Do I need a license to ride?"/>
           </template>
        </Faq>
        <Faq>
           <template v-slot:title>Safe driving</template>
           <template v-slot:questions>
            <Question question= "Should I wear a helmet?"/>
            <Question question= "How about the rules & regulations?"/>
            <Question question= "What if I damage my Scoot?"/>
           </template>

        </Faq>
      </section>
    </main>
  </div>
</template>

<script>
import Header from './../components/Header'
import Article from './../components/Article'
import Values from './../components/Values'
import Faq from './../components/Faq'
import Question from './../components/Question'

  export default {
    components: {
      Header,
      Article,
      Values,
      Faq,
      Question
    },
    mounted () {
        console.log(Article)
      },
    methods: {
      mounted () {
        console.log(Article)
      }
    }
  }
</script>

<style lang="scss" scoped>
$darkNavy: #495567;

  .about {
    .header-about {
      background-image: url('./../../public/images/about-hero-desktop.jpg');
    }
    main {
      overflow: hidden;
      width: 100%;
      margin: auto;
      margin: auto;
   
      .contain-article {
        width: 100%;
        margin-bottom: 120px;
        .article-digital-era { 
          width: 1619px;
          svg{
            position: absolute;
            right: 0;
            bottom: 38px;
          }
        }
        .article-better-living { 
          width: 1660px;
          svg{
            position: absolute;
            top: 8px;
            right: 260px;
          }
        }
      }
      .our-values {
        margin: auto;
        margin-bottom: 120px;
      }
      .faq {
        width: 1110px;
        height: 990px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        margin: auto;
        h2 {
          color: $darkNavy;
          text-align: center;
          margin: 0;
          
        }
      }
    }
  }
     
  @media screen and (max-width: 1200px) {
    .about {
      main {
        .contain-article {
          margin-bottom: 72px;
        }
        .faq {
          width: 689px;
          height: 1166px;
          align-items: center;
        }
      }
    }
  }

  @media screen and (max-width: 600px) {
    .about {
      main {
        .faq {
          width: 311px;
          height: 1382px;
        }
      }
    }
  }
</style>