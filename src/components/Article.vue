<template>
    <section class="article">
        <article class="text-article">
            <h2><slot name="title"></slot></h2>
            <p><slot name="text"></slot></p>
            <Button text="Learn More"/>
        </article>
        <figure>
            <div class="image-article">
                <slot name="photo"></slot>
            </div>
            <svg xmlns="http://www.w3.org/2000/svg" width="445" height="445"><circle cx="302.5" cy="222.5" r="222.5" fill="#E5ECF4" fill-rule="evenodd" transform="translate(-80)"/></svg>
            <slot name="decoration" class="decoration"></slot>
        </figure>
        
    </section>
</template>

<script>
import Button from './../components/Button'

    export default {
        props: ['title', 'text', 'image'],
        components: {
            Button,
        }
    }
</script>

<style lang="scss" scoped>
    $darkNavy: #495567;
    $dimGrey: #939CAA;
    .article {
        height: 445px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 160px;
        article {
            width: 445px;
            height: 313px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            h2 {
                width: 518px;
                color: $darkNavy;
                height: 96px;
            }
            p {
                color: $dimGrey;
                height: 100px;
                width: 445px;
            }
            h2, p {
                margin: 0;
            }
        }
        figure {
            width: 954px;
            display: flex;
            justify-content: space-between;
            margin: 0;
            position: relative;
            .image-article {
                width: 445px;
                height: 445px;
                img {
                    width: 100%;
                    border-radius: 50%;
                }
            }
        }
        .decoration {
            position: absolute;
        }
    }
    .article:nth-child(2n+1) {
        width: 1619px;  
        margin-left: 165px;
    }

    .article:nth-child(2n) {
      margin-left: -325px;
      flex-direction: row-reverse;
      figure {
        flex-direction: row-reverse;
      }
    }

</style>