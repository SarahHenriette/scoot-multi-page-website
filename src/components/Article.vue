<template>
    <section class="article">
        <article class="text-article">
            <h2><slot name="title"></slot></h2>
            <p><slot name="text"></slot></p>
            <slot name="button"></slot>
        </article>
        <figure>
            <div class="image-article">
                <slot name="photo"></slot>
            </div>
            <svg xmlns="http://www.w3.org/2000/svg" class="circle" width="445" height="445"><circle cx="302.5" cy="222.5" r="222.5" fill="#E5ECF4" fill-rule="evenodd" transform="translate(-80)"/></svg>
            <slot name="decoration" class="decoration"></slot>
        </figure>
        
    </section>
</template>

<script>
    export default {
        props: ['textButton'],
        components: {
        },
        data () {
            return {
            }
        }
    }
</script>

<style lang="scss" scoped>
    $darkNavy: #495567;
    $dimGrey: #939CAA;
    .article {
        height: 445px;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        article {
            width: 445px;
            height: auto;
            display: flex;
            flex-direction: column;
            h2 {
                width: 518px;
                color: $darkNavy;
                height: 96px;
                margin: 0;
            }
            p {
                color: $dimGrey;
                height: 100px;
                width: 445px;
                margin: 24px 0 40px 0;
            }
    
        }
        figure {
            width: 954px;
            display: flex;
            justify-content: space-between;
            margin: 0 ;
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

    .contain-article:nth-child(2n+1) .article {
        article {
            margin-right: 220px;
        }
    }
    .contain-article:nth-child(2n) .article {
        flex-direction: row-reverse;
        justify-content: center;
        article {
            margin-left: 220px;
        }
        figure {
            flex-direction: row-reverse;
        }
    }

    @media screen and (max-width: 1245px) { 
        .article {
            height: 805px;
            flex-direction: column-reverse;
            article {
                align-items: center;
                h2 {
                   text-align: center;
                }
                p {
                    text-align: center;
                    width: 573px;
                    height: 75px;
                    margin: 40px 0;
                }
                .btn-article {
                    margin: 0 auto;
                }
            }
        }
        .contain-article:nth-child(2n+1) .article {
            align-items: flex-start;
            article {
                margin-right: 0;
                margin-top: 56px;
            }
        }
         .contain-article:nth-child(2n) .article {
            flex-direction: column-reverse;
            align-items: flex-end;
            margin-left: -65%;
           article {
            margin-left: 0;
            margin-top: 56px;
           }
        }
        
    }

  @media screen and (max-width: 530px) {
        .article {
            height: 698px;
            article {
                width: 311px;
                height: 331px;
                h2 {
                    width: 355px;
                    height: 64px;
                    font-size: 32px;
                    line-height: 32px;
                }
                p {
                    width: 311px;
                    height: 150px;
                    font-size: 15px;
                    line-height: 25px;
                }
            }
            figure {
                .image-article {
                    width: 311px;
                    height: 311px;
                }
                .circle {
                    display: none;
                }
            }
        }
    }

</style>