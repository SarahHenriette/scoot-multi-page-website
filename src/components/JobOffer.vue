<template>
<article class="job">
    <div class="text-job">
        <h4>{{ name }}</h4>
        <p>{{ location }}</p>
    </div>
    <Button text="Apply" class="btn-article" />    
</article>
</template>

<script>
import Button from './../components/Button'

export default {
    props: {
        name: String,
        location: String
    },
    components: {
        Button
    }
}
</script>
    
<style lang="scss" scoped>
$snow: #F2F5F9;
 $darkNavy: #495567;
  $dimGrey: #939CAA;
    .job {
        width: 100%;
        height: 128px;
        background-color: $snow;
        display: flex;
        justify-content: space-between;
        align-items: center;
        .text-job {
            margin-left: 40px;
            h4, p {
                margin: 0;
            }
            h4 {
                color: $darkNavy;
            }
            p {
                color: $dimGrey;
            }
        }
        .btn-article {
            margin-right: 64px;
        }
    }

      @media screen and (max-width: 720px) {
          .job{
              height: 190px;
              flex-direction: column;
              justify-content: center;
              
              .text-job {
                    margin-left: 0;
                    height: 53px;
                    margin-bottom: 16px;
                h4, p {
                    text-align: center;
                }
                h4 {
                    font-size: 18px!important;
                }
              }
              .btn-article {
                  margin-right: 0;
                  width: 247px;
              }
          }
      }
</style>