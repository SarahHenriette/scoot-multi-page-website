<template>
    <header>
      <div class="text-header">
        <h1>Scooter sharing made simple</h1>
        <p>Scoot takes the hassle out of urban mobility. Our bikes are placed in convenient locations in each of our cities. Use our app to locate the nearest bike, unlock it with a tap, and you’re away!</p>
        <Button text ="Get Scootin" class="btn-home"/>
      </div>
      <svg xmlns="http://www.w3.org/2000/svg" class="background-line" width="203" height="15"><path fill="none" stroke="#FCB72B" stroke-width="15" d="M203 7.5H.5"/></svg>
      <svg xmlns="http://www.w3.org/2000/svg" class="background-right-arrow" width="452" height="151"><g fill="none" fill-rule="evenodd" stroke="#FCB72B" stroke-linejoin="bevel" stroke-width="15"><path d="M407.952 145.444l38.426-38.426-38.426-38.426"/><path d="M0 8h270.115v99.369h176.263"/></g></svg>
      <svg xmlns="http://www.w3.org/2000/svg" class="background-circles" width="234" height="63"><g fill="none" fill-rule="evenodd"><circle cx="31" cy="31.5" r="29.5" stroke="#FFF" stroke-width="3"/><circle cx="117" cy="31.5" r="29.5" stroke="#FFF" stroke-width="3"/><circle cx="203" cy="31.5" r="31" fill="#FFF"/></g></svg>
    </header>
</template>

<script>
import Button from './../components/Button'
    export default {
        components: {
            Button,
        }
    }
</script>

<style lang="scss" scoped>
$white: #FFF;
$lightGrey: #E5ECF4;

  header {
    width: 100%;
    height: 650px;
    background-image: url('./../../public/images/home-hero-desktop.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
    overflow: hidden;
    .text-header, .background-line, .background-right-arrow, .background-circles {
      position: absolute;
    }
    .text-header {
      width: 562px;
      height: 345px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      top: 153px;
      left: 165px;
      h1, p {
        color: $white;
        margin: 0;
      }
      h1 {
        width: 100%;
        height: 112px;
      }
      p {
        width: 405px;
        height: 100px;
      }
      p, .btn-home {
        margin-left: 113px;
      }
    }
    .background-line {
      bottom: 295px;
    }
    .background-right-arrow {
      bottom: 157px;
      right: 279px;
    }
    .background-circles {
      right: -48px;
      bottom: 164.5px;
    }
  }

    @media screen and (max-width: 1435px) {
    header {
      background-image: url('./../../public/images/home-hero-tablet.jpg');
      .text-header {
        width: 573px;
        height: 296px;
        top: 137px;
        left: 0;
        right: 0;
        margin: auto;
        p {
          width: 100%;
          height: 75px;
        }
        p, .btn-home {
          margin-left: 0;
        }
        h1, p {
          text-align: center;
        }
        .btn-home {
          margin: 0 auto;
        }
      }
      .background-line {
        display: none;
      }
      .background-right-arrow {
        left: -127px;
        bottom: 39px;
      }
      .background-circles {
        right: -31px;
        bottom: 45px;
      }
    }
  }

  @media screen and (max-width: 700px) {
       header {
      background-image: url('./../../public/images/home-hero-mobile.jpg');
      height: 650px;
      .text-header {
        width: 311px;
        height: 356px;
        top: 115px;
        left: 0;
        right: 0;
        margin: auto;
        h1 {
          font-size: 40px!important;
          line-height: 40px!important;
          height: 120px;
        }
        p {
          width: 100%;
          height: 125px;
        }
        h1, p {
          text-align: center;
        }
        .btn-home {
          margin: 0 auto;
        }
      }
      .background-right-arrow {
        left: -312px;
        bottom: 34px;
      }
      .background-circles {
       display: none;
      }
    }

  }
</style>