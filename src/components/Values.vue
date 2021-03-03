<template>
    <section class="our-values">
        <h2>{{ title }}</h2>
        <div class="contain-our-values">
          <BreakPointsValues>
                <template v-slot:image><img src="images/our-tech.jpg" alt="main tenant un telephone"></template>
                <template v-slot:number>01</template>
                <template v-slot:title>Our tech</template>
                <template v-slot:text>We’re using cutting edge technology to drive accessible urban transportation forward. Our fully electric scooters are a joy to ride!</template>
          </BreakPointsValues>
            <BreakPointsValues>
                <template v-slot:image><img src="images/our-integrity.jpg" alt="homme sur un scooter"></template>
                <template v-slot:number>02</template>
                <template v-slot:title>Our integrity</template>
                <template v-slot:text>We are fully committed to deliver a great yet safe, sustainable micro-mobility experience in every city we serve.</template>
          </BreakPointsValues>
            <BreakPointsValues>
                <template v-slot:image><img src="images/our-community.jpg" alt="groupe de personnes traversant les piétons"></template>
                <template v-slot:number>03</template>
                <template v-slot:title>Our community</template>
                <template v-slot:text>We support every community we serve. All workers are paid a living wage based on their location and are Scoot employees.</template>
          </BreakPointsValues>
        </div>

    </section>
</template>

<script>
import BreakPointsValues from './../components/BreakPointsValues'

    export default {
        props: ['title'],
        components: {
            BreakPointsValues
        }
    }
</script>

<style lang="scss" scoped>
$darkNavy: #495567;
     .our-values {
        width: 1110px;
        height: 608px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        h2 {
            margin: 0;
            text-align: center;
            color: $darkNavy;
        }
        .contain-our-values {
            display: flex;
            justify-content: space-between;
        }

      }

      @media screen and (max-width: 1110px) {
          .our-values {
              width: 457px;
              height: 1584px;
              .contain-our-values {
                  flex-direction: column;
                  align-items: center;
              }
          }
      }
         @media screen and (max-width: 415px) {
          .our-values {
              width: 311px;
              height: 1535px;
              h2 {
                  font-size: 32px;
              }
          }
      }
</style>