<template>
     <article class="how-it-works">
          <h3><slot name="title">How it works</slot></h3>
          <div class="contain-questions">
              <slot name="questions"></slot>
          </div>
    </article>
</template>

<style lang="scss" scoped>
$darkNavy: #495567;
article {
    width: 100%;
    height: 407px;
    display: flex;
    justify-content: space-between;
    h3 {
        color: $darkNavy;
        margin: 0;
    }
    .contain-questions {
        width: 730px;
        height: 407px;
    }
}
@media screen and (max-width: 1200px) {
  article {
      flex-direction: column;
      width: 689px;
      height: 503px;
      h3 {
          text-align: center;
      }
    .contain-questions {
        width: 100%;
        height: 423px;
    }
  }
}

@media screen and (max-width: 600px) {
    article {
      width: 311px;
      height: 627px;
      h3 {
          font-size: 24px!important;
          line-height: 28px!important;
      }
    .contain-questions {
        height: 567px;
    }
  }
}
</style>