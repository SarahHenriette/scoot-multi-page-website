<template>
    <footer>
        <ul class="links-footer">
            <li><router-link to="/"><Logo class="logo-footer"/></router-link></li>
            <li><router-link to="/about">About</router-link></li>
            <li><router-link to="/location">Location</router-link></li>
            <li><router-link to="/location">Careers</router-link></li>
        </ul>
        <ul class="links-social-icon-footer">
            <li><a href="https://www.facebook.com/"><img src="icons/facebook.svg" alt="f de couleur bleu"></a></li>
            <li><a href="https://twitter.com/home?lang=fr"><img src="icons/twitter.svg" alt="pictogramme oiseau"></a></li>
            <li><a href="https://www.instagram.com/?hl=fr"><img src="icons/instagram.svg" alt="pictogramme d'appareil photo"></a></li>
        </ul>
    </footer>
</template>

<script>
import Logo from './Logo'
export default {
    components: {
        Logo
    }
}
</script>

<style lang="scss" scoped>
  $darkGrey: #333A44;

    footer {
        width: 100%;
        height: 96px;
        background-color: $darkGrey;
        display: flex;
        justify-content: space-between;
        align-items: center;
        .links-footer, .links-social-icon-footer {
            display: flex;
            justify-content: space-between;
        }
        .links-footer {
            width: 417px;
            height: 29px;
            margin-left: 168px;
            .logo-footer {
                fill: #FFF;
                margin-right: 58px;
            }
        }
        .links-social-icon-footer {
            width: 120px;
            height: 24px;
            margin-right: 165px;
            svg {
                fill: #FCB72B;
                transition: fill .5s linear;
                &:hover {
                    fill: #FFF;
                }
            }
        }
    }

    @media screen and (max-width: 1110px) {
        footer {
            .links-footer {
                margin-left: 39px;
            }
            .links-social-icon-footer {
                margin-right: 40px;
            }
        }
    }

    @media screen and (max-width: 700px) {
        footer {
            height: 438px;
            flex-direction: column;
            .links-footer {
                flex-direction: column;
                margin-top: 64px;
                width: 100%;
                height: 176px;
                margin-left: 0;
                .logo-footer {
                    margin-right: 0;
                }
            }
            .links-social-icon-footer {
                margin-right: 0;
                margin-bottom: 88px;
            }
        }
    }
    
</style>