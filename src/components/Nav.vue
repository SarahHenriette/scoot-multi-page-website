<template>
    <div id="nav">
        <ul class="links-nav">
            <li><router-link to="/"><Logo class="logo-nav"/></router-link></li>
            <li><router-link to="/about">About</router-link></li>
            <li><router-link to="/location">Location</router-link></li>
            <li><router-link to="/location">Careers</router-link></li>
        </ul>
        <Button text ="Get Scootin" class="btn-nav"/>
        <NavMobile class="nav-mobile"/>
    </div>
</template>

<script>
import Button from './Button'
import NavMobile from './NavMobile'
import Logo from './Logo'

export default {
    components: {
        Button,
        NavMobile,
        Logo
    }
}
</script>

<style lang="scss">

#nav, ul {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
#nav {
    width: 100%;
    height: 96px;
    .links-nav {
        width: 415px;
        height: 28px;
        margin-left: 169px; 
        .logo-nav {
            fill: #495567;
            margin-right: 58px;
        }       
    }
    .btn-nav {
        margin-right: 165px;
    }
    .nav-mobile {
        display: none;
        width: 100%;
    }
    #background-menu-nav-mobile {
    }
    #menu-nav-mobile {
    }
}

@media screen and (max-width: 1110px) {
    #nav {
        .links-nav {
            margin-left: 39px;
        }
        .btn-nav {
            margin-right: 40px;
        }
    }
}

@media screen and (max-width: 700px) {
       #nav {
           height: 64px;
            .links-nav, .btn-nav {
                display: none;
            }
            .nav-mobile {
                display: flex;
            }
        }
}
</style>