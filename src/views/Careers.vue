<template>
  <div class="careers">
    <Header text="Careers" class="header-careers"/>
    <main>
      <div class="contain-article contain-join-us">
        <Article class="article-join-us">
          <template v-slot:title>Care to join our mission?</template>
          <template v-slot:text>We’re always looking for ambitious individuals to help us on our journey. If you’re passionate about our mission to provide clean, accessible transport to improve urban living we want to hear from you!</template>
          <template v-slot:photo><img src="images/join-us.jpg" alt="jeune homme se tenant de ses interlocuteurs et exposant ses idées"></template>
          <template v-slot:decoration><svg xmlns="http://www.w3.org/2000/svg" width="741" height="151"><g fill="none" fill-rule="evenodd" stroke="#FCB72B" stroke-linejoin="bevel" stroke-width="15"><path d="M740.969 8H182.854v99.369H6.591"/><path d="M44.64 145.64L6.214 107.214 44.64 68.787"/></g></svg></template>
          <template v-slot:button><Button text="Say Hello" class="btn-article"/></template>
      </Article>
     </div>

     <Values title="Why join us?" class="why-join-us" />

     <section class="job-offer">
        <JobOffer name="General Manager" location="Jakarta, Indonesia"/>
        <JobOffer name="UI/UX Designer" location="Yokohama, Japan"/>
        <JobOffer name="Blog Content Copywriter" location="New York, United States"/>
        <JobOffer name="Graphic Designer" location="New York, United States"/>
        <JobOffer name="Fleet Supervisor" location="Jakarta, Indonesia"/>
        <JobOffer name="UX Analyst" location="London, United Kingdom"/>
      </section>
    </main>
  </div>
</template>

<script>
import Header from './../components/Header'
import Article from './../components/Article'
import Button from './../components/Button'
import Values from './../components/Values'
import JobOffer from './../components/JobOffer'

  export default {
    components: {
      Header,
      Article,
      Button,
      Values,
      JobOffer
    }, 
    data () {
      return {
     
      }
    }
  }
</script>

<style lang="scss" scoped>
  .careers {
    .header-careers {
      background-image: url('./../../public/images/careers-locations-hero-desktop.jpg');
    }
    main {
      overflow: hidden;
      width: 100%;
      margin: auto;
      .contain-join-us {
        width: 100%;
        margin-bottom: 160px;
        .article-join-us { 
          width: 1619px;
          svg{
            position: absolute;
            left: 0;
            bottom: 0;
          }
        }
      }
      .why-join-us {
        margin: auto;
        margin-bottom: 120px;
      }

      .job-offer {
        width: 1110px;
        height: 888px;
        margin: auto;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        margin-bottom: 120px;
      }
    }
  }

  @media screen and (max-width: 1110px) {
    .careers {
      
      main {
        .job-offer {
          width: 689px;
          height: 848px;
        }
      }
    }
  }
  @media screen and (max-width: 720px) {
    .careers {
      main {
        .job-offer {
          width: 311px;
          height: 1220px;
        }
      }
    }
  }
</style>