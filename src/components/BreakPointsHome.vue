<template>
    <section id="break-points">
      <div class="contain-break-points">
        <BreakPoints1 image="icons/locate.svg" title="Locate with app" text="Use the app to find the nearest scooter to you. We are continuously placing scooters in the areas with most demand, so one should never be too far away." />
        <BreakPoints1 image="icons/scooter.svg" title="Pick your scooter" text="We show the most important info for the scooters closest to you. So you know how much charge they have left and can see roughly how much it will cost.." />
        <BreakPoints1 image="icons/ride.svg" title="Enjoy the ride" text="Scan the QR code and the bike will unlock. Retract the cable lock, put on a helmet, and you’re off! Always lock bikes away from walkways and accessibility ramps." />
      </div>
      <span class="background-line"></span>
    </section>
</template>

<script>
import BreakPoints1 from './../components/BreakPoints1'

    export default {
        components: {
            BreakPoints1,
        }
    }
</script>

<style lang="scss" scoped>
$white: #FFF;
$lightGrey: #E5ECF4;
#break-points {
    width: 1274.5px;
    height: 291px;
    margin: 160px 0 200px 0;
    display: flex;
    justify-content: flex-end;
    position: relative;
    .contain-break-points {
      width: 1110px;
      display: flex;
      position: absolute;
      justify-content: space-between;
      z-index: 10;
    }
    .background-line {
      position: absolute;
      height: 15px;
      width: 973px;
      background-color: $lightGrey;
      left: 0;
      top: 44px;
    }
  }

    @media screen and (max-width: 1300px) {
    #break-points {
      width: 573px;
      height: 470px;
      margin: 122px auto 145px auto;
      .contain-break-points {
        width: 100%;
        height: 100%;
        margin: auto;
      }
      .background-line {
        width: 15px;
        height: 513px;
        left: 43px;
        top: -121px;
      }
    }
    #break-points, #break-points .contain-break-points {
      flex-direction: column;
    }
  }

    @media screen and (max-width: 700px) {
     #break-points {
       width: 311px;
       height: 792px;
        margin: 120px auto 120px auto;
      .contain-break-points {
        width: 100%;
        height: 100%;
        margin: auto;
      }
      .background-line {
        display: none;
      }
    }
    #break-points, #break-points .contain-break-points {
      flex-direction: column;
    }
  }
</style>