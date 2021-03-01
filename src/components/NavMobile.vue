<template>
        <div>
            <div id="nav-mobile">
                <div v-if="menuBurger" @click="displayMenuBurger" class="contain-icon"><MenuBurger/></div>
                <div v-else @click="hideMenuBurger" class="contain-icon"><Close/></div>
                <Logo  @click="displayMenuBurger" class="logo-nav-mobile"/>
            </div>
            <div class="background-menu-nav-mobile" :class="active"></div>
            <div class="menu-nav-mobile" :class="active">
                <ul class="links-nav-mobile">
                    <li><router-link to="/about">About</router-link></li>
                    <li><router-link to="/location">Location</router-link></li>
                    <li><router-link to="/location">Careers</router-link></li>
                </ul>
                <Button text ="Get Scootin" class="btn-nav-mobile"/>
            </div>
        </div>
</template>

<script>
import Button from './Button'
import Logo from './Logo'
import MenuBurger from './MenuBurger'
import Close from './Close'

    export default {
        components: {
            Button,
            Logo,
            MenuBurger,
            Close
        },
        data () {
            return {
                menuBurger: true,
                active: ''
            }
        },
        methods: {
            displayMenuBurger() {
                this.menuBurger = false
                this.active = "active"
            },
            hideMenuBurger () {
                this.menuBurger = true
                this.active = ''
            }
        }
    }
</script>
<style lang="scss" scoped>
  $lightGrey: #E5ECF4;

    #nav-mobile {
        width: 100%;
        padding: 0 32px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        .contain-icon {
            height: 25px;
            width: 25px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .logo-nav-mobile {
            margin: auto;
            fill: #495567;
        }
    }
    
    .background-menu-nav-mobile, .menu-nav-mobile {
        display: none;
        height: 100%;
        position: absolute;
        top: 64px;
        z-index: 10;
    }
    .background-menu-nav-mobile {
        width: 100%;
        background-color: #000;
        opacity: 0.9;
    }
    .menu-nav-mobile {
        width: 256px;
        background-color: #333A44;
        .links-nav-mobile {
            width: 89px;
            height: 123px;
            flex-direction: column;
            justify-content: space-between;
            align-items: flex-start;
            margin-top: 64px;
            margin-left: 32px;
            li a {
                color: $lightGrey;
            }
        }
        .btn-nav-mobile {
            position: absolute;
            bottom: 24px;
            left: 0;
            right: 0;
            margin: auto;
        }
    }

    .active {
        display: flex;
    }
    
</style>