<template>
  <div class="location">
    <Header text="Location" class="header-location"/>
    <section class="map">
      <PointerMap city="New York" class="new-york" />
      <PointerMap city="London" class="london" />
      <PointerMap city="Yokohama" class="yokohama" />
      <PointerMap city="Jakarta" class="jakarta" />
    </section>
    <section class="pointer-mobile">
      <div class="contain-city"><p>New York</p></div>
      <div class="contain-city"><p>London</p></div>
      <div class="contain-city"><p>Yokohama</p></div>
      <div class="contain-city"><p>Jakarta</p></div>
    </section>

    <section class="your-city">
      <h2>Your City Not Listed?</h2>
      <p>If you’d like to see Scoot in your hometown, be sure to let us know. We track requests and plan launches based on demand. Feel free to message us by clicking the link or messaging us on social.</p>
      <Button text="Message Us"/>
    </section>
  </div>
</template>

<script>
import Header from './../components/Header'
import Button from './../components/Button'
import PointerMap from './../components/PointerMap'

  export default {
    components: {
      Header,
      Button,
      PointerMap
    }
  }
</script>

<style lang="scss" scoped>
$darkNavy: #495567;
$dimGrey: #939CAA;
$lightYellow: #FFF4DF;

  .location {
    .header-location {
      background-image: url('./../../public/images/careers-locations-hero-desktop.jpg');
    }
    .map {
      width: 1110px;
      height: 543px;
      margin: auto;
      margin-bottom: 120px;
      background-image: url('./../../public/images/world-map-desktop.png');
      background-repeat: no-repeat;
      background-size: contain;
      position: relative;
      .new-york {
        left: 147px;
        top: 71.4px;
      }
      .london {
        left: 393px;
        top: 18px;
      }
      .yokohama {
        right: 65px;
        top: 78px;
      }
      .jakarta {
        right: 142px;
        bottom: 203.8px;
      }
    }

    .pointer-mobile {
      display: none;
      width: 311px;
      height: 336px;
      flex-direction: column;
      justify-content: space-between;
      margin: 0 auto 72px auto;
      .contain-city {
        width: 100%;
        height: 72px;
        background-color: $lightYellow;
        display: flex;
        justify-content: center;
        align-items: center;
        p {
          font-size: 24px!important;
          color: $darkNavy;
          font-weight: 700;
        }
      }
    }

    .your-city {
      width: 1111px;
      height: 100px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin: auto;
      margin-bottom: 120px;
      h2 {
        width: 351px;
        height: 96px;
        color: $darkNavy;
        margin: 0;
      }
      p  {
        width: 445px;
        height: 100px;
        color: $dimGrey;
        margin: 0;
      }
    }
  }

  @media screen and (max-width: 1200px) {
    .location {
      .map {
        width: 689px;
        height: 337px;
        margin-bottom: 64px;
        .new-york {
          left: 98px;
          top: 52px;
        }
        .london {
          left: 246px;
          top: 26px;
        }
        .yokohama {
          right: 41px;
          top: 67px;
        }
        .jakarta {
          right: 92px;
          bottom: 129px;
        }
      }
      .your-city {
        width: 573px;
        height: 304px;
        flex-direction: column;
        h2, p {
          text-align: center;
        }
        h2 {
          width: 457px;
          height: 96px;
        }
        p {
          width: 573px;
          height: 75px;
        }
      }
    }
  }

  @media screen and (max-width: 700px) {
    .location {
      .map {
        width: 311px;
        height: 152px;
        margin-bottom: 40px;
        .new-york {
          left: 67px;
          top: 33px;
        }
        .london {
          left: 128px;
          top: 18px;
        }
        .yokohama {
          right: 37px;
          top: 40px;
        }
        .jakarta {
          right: 58px;
          bottom: 49.8px;
        }
      }
      .pointer-mobile {
        display: flex;
      }
      .your-city {
        width: 311px;
        height: 306px;
        h2 {
          font-size: 32px;
          line-height: 32px;
          width: 311px;
          height: 64px;
        }
        p {
          width: 311px;
          height: 125px;
        }
      }
    }
  }
</style>