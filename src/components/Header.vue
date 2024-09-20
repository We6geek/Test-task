<script setup>
import Popup from '@/components/Popup.vue';
</script>

<script>
export default {
    data() {
        return {
            isMenuActive: false
        };
    },
    methods: {
        toggleMenu() {
            this.isMenuActive = !this.isMenuActive;
        }
    },

    components: {
        Popup
    },
    methods: {
        openPopup() {
        this.$refs.popup.openPopup();
        }
    }
};
</script>

<template>
    <header>
        <div class="header d-flex d-flex-justify-center">
            <div class="header-content d-flex d-flex-justify-between">
                <div class="header-navigation d-flex d-flex-align-center">
                    <a href="#"><img src="@/assets/images/logo.svg" alt="Logotype"></a>
                    <nav class="d-flex d-flex-align-center">
                        <div :class="['nav-menu d-flex d-flex-align-center', { 'active': isMenuActive }]">
                            <div class="close-menu" @click="toggleMenu">✕</div>
                            <ul class="d-flex" id="nav-ul">
                                <a href="#"><li>Games</li></a>
                                <a href="#"><li>Contact Us</li></a>
                                <a href="#"><li>Terms of Use</li></a>
                                <a href="#"><li>About</li></a>
                            </ul>
                        </div>
                    </nav>
                </div>
                <div class="header-account d-flex d-flex-align-center">
                    <a class="d-flex d-flex-align-center" href="#" @click="openPopup"><p>Sign up</p></a>
                    <a class="d-flex d-flex-align-center" href="#"><button class="button" type="button">Log in</button></a>
                    <div class="burger-menu" @click="toggleMenu">☰</div>
                </div>
            </div>

            <div v-if="isMenuActive" class="overlay" @click.self="toggleMenu"></div>

            <div>
                <!-- Компонент попапа -->
                <Popup ref="popup" />
            </div>
        </div>
    </header>
</template>

<style lang="scss">
@use "@/assets/breakpoints";

.header {
    padding: 12px 0;
    background-color: var(--blue-transparent);
    backdrop-filter: blur(10px);
    width: 100%;
    max-height: 72px;
    position: fixed;
    z-index: 10;

    &-content {
        width: 100% !important;
        max-width: 1040px;
    }

    &-navigation {
        grid-gap: 64px;

        img {
            width: 48px;
            height: 48px;
        }

        .nav-menu {
            transform: none;
            
            ul {
                display: flex;
                grid-gap: 36px;
                margin: 0;
                padding: 0;
                list-style-type: none;

                a {
                    position: relative !important;
                    text-decoration: none;
                    color: var(--white);
                    width: auto !important;
                }

                li {
                    width: auto !important;
                    font-weight: 600;
                }

                li:hover {
                    background-image: linear-gradient(69deg, rgba(250, 0, 255, 1) 0%, rgba(72, 112, 255, 1) 100%);
                    -webkit-background-clip: text;
                    -webkit-text-fill-color: transparent;
                }

                li:hover::before {
                    content: "";
                    position: absolute;
                    bottom: -26px;
                    left: 0;
                    width: 100%;
                    height: 4px;
                    border-radius: 4px 4px 0 0;
                    background-image: linear-gradient(69deg, rgba(250, 0, 255, 1) 0%, rgba(72, 112, 255, 1) 100%);
                    box-shadow: 0 4px 16px 0 rgba(138, 97, 255, 0.6);
                }
            }
        }

        .close-menu {
            display: none;
            position: absolute;
            top: 10px;
            right: 20px;
            font-size: 30px;
            cursor: pointer;
            color: var(--white);
        }
    }

    &-account {
        grid-gap: 16px;

        a {
            color: var(--white);
            font-size: 18px;
            font-weight: 600;

            button {
                height: 44px;
                font-weight: 600;
            }
        }

        a:first-child:hover {
            background-image: linear-gradient(69deg, rgba(250, 0, 255, 1) 0%, rgba(72, 112, 255, 1) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .burger-menu {
            font-size: 30px;
            cursor: pointer;
            color: var(--white);
            z-index: 20;
            display: none !important;
        } 
    }

    .overlay {
        position: fixed;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
        background-color: rgba(0, 0, 0, 0.5);
        z-index: 15;
    }

    @include breakpoints.media-under-xl {
        &-content {
            max-width: 80% !important;
        }
    }

    @include breakpoints.media-under-lg {
        &-content {
            width: 85%;
        }

        &-navigation {
            .burger-menu {
                display: block;
            }

            .nav-menu {
                display: block;
                position: fixed;
                top: 0;
                right: 0;
                width: 250px;
                height: 100vh;
                background-color: #333;
                flex-direction: column;
                padding: 60px 20px;
                transform: translateX(100%);
                transition: transform 0.3s ease;
                z-index: 99;
            }

            .nav-menu.active {
                display: flex;
                transform: translateX(0);

                li {
                    font-size: 18px;
                }

                ul {
                    flex-direction: column;
                    grid-gap: 20px;
                }
            }

            a {
                width: auto !important;
                display: block;
                color: var(--white);
                padding: 10px 0;
            }
            
            li {
                width: auto !important;
            }

            li:hover::before {
                width: auto;
            }

            .close-menu {
                display: block;
            }
        }

        &-account {
            .burger-menu {
                display: block !important;
            }
        }
    }

    @include breakpoints.media-under-xs {
        &-navigation {
            grid-gap: 16px;
        }
        &-account {
            button {
                width: 70px;
            }
        }
    }
}
</style>
