<template>
    <header>
        <h2> {{ text }} </h2>
        <svg xmlns="http://www.w3.org/2000/svg" class="background-circles" width="234" height="63"><g fill="none" fill-rule="evenodd"><circle cx="31" cy="31.5" r="29.5" stroke="#FFF" stroke-width="3"/><circle cx="117" cy="31.5" r="29.5" stroke="#FFF" stroke-width="3"/><circle cx="203" cy="31.5" r="31" fill="#FFF"/></g></svg>
    </header>
</template>

<script>
    export default {
        props: ['text']
    }
</script>

<style lang="scss" scoped>
$white: #FFF;

    header {
        width: 100%;
        height: 200px;
        display: flex;
        align-items: center;
        position: relative;
        overflow: hidden;
        margin-bottom: 120px;
        h2, .background-circles {
            position: absolute;
        }
        h2 {
            color: $white;
            left: 165px;
        }
        .background-circles {
            right: -31px;
        }
    }

    @media screen and (max-width: 1110px) {
        header {
            h2 {
                left: 97px;
            }
        }
    }

    @media screen and (max-width: 700px) {
        header {
            margin-bottom: 72px;
            h2 {
                text-align: center;
                left: 0;
                right: 0;
                margin: auto;
            }
            .background-circles {
                display: none;
            }
        }
    }
</style>