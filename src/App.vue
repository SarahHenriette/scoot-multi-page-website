<template>
  <div id="app">
    <Nav/>
    <router-view/>
    <SignUp/>
    <Footer/>
  </div>
</template>

<script>
import Nav from './components/Nav'
import Footer from './components/Footer'
import SignUp from './components/SignUp'

export default {
  components: {
    Nav,
    Footer,
    SignUp
  }
}
</script>

<style lang="scss">
 @import url('https://fonts.googleapis.com/css2?family=Lexend+Deca&family=Space+Mono:wght@700&display=swap');

  $spaceMono:'Space Mono', monospace;
  $lexend: 'Lexend Deca', sans-serif;

  $yellow: #FCB72B;
  $darkNavy: #495567;
  $dimGrey: #939CAA;
  $lightGrey: #E5ECF4;
  $darkGrey: #333A44;
  $snow: #F2F5F9;
  $lightYellow: #FFF4DF;
  $white: #FFF;

  body {
    margin: 0;
  }

  h1, h2, h3, h4, a, button {
    font-family: $spaceMono;
  }

  h1 {
    font-size: 56px;
    line-height: 56px;
  }

  h2 {
    font-size: 48px;
    line-height: 48px;
    letter-spacing: 2.14px;
  }

  h3 {
    font-size: 40px;
    line-height: 48px;
    letter-spacing: 1.79px;
  }

  h4 {
    font-size: 24px;
    line-height: 28px;
    letter-spacing: 1.07px;
  }

  p {
    font-family: $lexend;
    font-size: 15px;
    line-height: 25px;
  }

  ul {
    padding-left: 0;
    margin: 0;
  }

  li {
    list-style-type: none;
  }

  a {
    font-size: 15px;
    line-height: 25px;
    font-weight: bold;
    color: $dimGrey;
    text-decoration: none;
    transition: color .5s ease;
    &:hover {
      color: $darkNavy;
    }
  }

//affichage des "articles" de la page home  

  main {
    .contain-article:nth-child(2n+1) {
      .article {
        margin-left: 165px;
      }
    }

    .contain-article:nth-child(2n) {
      display: flex;
      justify-content: flex-end;
      .article {
        margin-right: 165px
      }
    }
  }

  @media screen and (max-width: 1435px) {
    main {
      width: 100%;
      .contain-article:nth-child(2n+1) {
        .article {
          margin-left: 10%;
        }
      }
     .contain-article:nth-child(2n) {
        .article {
          margin-right: 10%;
        }
      }
    }
  }
    @media screen and (max-width: 1245px) {
    main {
      .contain-article:nth-child(2n+1) {
        .article {
          margin-left: 34%;
        }
      }
      .contain-article:nth-child(2n) {
        .article {
          margin-right: 28%;
        }
      }
    }
     
  }

  @media screen and (max-width: 780px) {
      main {
        .contain-article:nth-child(2n+1) {
          .article {
            margin-left: 23%;
          }
        }
        .contain-article:nth-child(2n) {
          .article {
            margin-right: 19%;
          }
        }
      }
  }

  @media screen and (max-width: 415px) {
    main {
      .contain-article:nth-child(2n+1) {
        .article {
          margin-left: 10%;
        }
      }
      .contain-article:nth-child(2n) {
        .article {
          margin-right: 8%;
        }
      }
    }
  }
</style>
