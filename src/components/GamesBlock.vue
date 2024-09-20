<script setup>
import ContactBlock from '@/components/ContactBlock.vue';

</script>

<template>
    <div class="games d-flex d-flex-colum d-flex-align-center">
        <div class="games-wrapper d-flex d-flex-colum">
            <div class="games-title d-flex d-flex-colum">
                <h2 class="h2">Our Games</h2>
                <div class="subtitle d-flex d-flex-justify-between">
                    <p class="subtitle-p">Get Virtual Welcome bonus after Sign Up</p>
                    <a href="#"><p class="p-semi">All games</p></a>
                </div>
            </div>
            <div class="games-catalog d-flex d-flex-align-center">
                <div class="catalog-slots">
                    <a href="#"><div class="slots-item">
                        <img src="../assets/images/games/gametype.2813.jpg" class="slots-item__img" alt="Slot preview">
                        <div class="item-text">
                            <h5 class="h5">Double Jackpot</h5>
                            <p class="item-text__p">NetentGames</p>
                        </div>
                    </div></a>
                    <a href="#"><div class="slots-item">
                        <img src="../assets/images/games/gametype.4298.jpg" class="slots-item__img" alt="Slot preview">
                        <div class="item-text">
                            <h5 class="h5">All Aboard: Dynamic corp</h5>
                            <p class="item-text__p">RushGameStudio</p>
                        </div>
                    </div></a>
                    <a href="#"><div class="slots-item">
                        <img src="../assets/images/games/gametype.4749.jpg" class="slots-item__img" alt="Slot preview">
                        <div class="item-text">
                            <h5 class="h5">Book Of Tombs</h5>
                            <p class="item-text__p">NetentGames</p>
                        </div>
                    </div></a>
                    <a href="#"><div class="slots-item">
                        <img src="../assets/images/games/gametype.4779.jpg" class="slots-item__img" alt="Slot preview">
                        <div class="item-text">
                            <h5 class="h5">Rudolph’s Ride</h5>
                            <p class="item-text__p">NetentGames</p>
                        </div>
                    </div></a>
                    <a href="#"><div class="slots-item">
                        <img src="../assets/images/games/gametype.5423.jpg" class="slots-item__img" alt="Slot preview">
                        <div class="item-text">
                            <h5 class="h5">Starburst XXXtreme</h5>
                            <p class="item-text__p">StarBurst Inc.</p>
                        </div>
                    </div></a>
                    <a href="#"><div class="slots-item">
                        <img src="../assets/images/games/gametype.1882.jpg" class="slots-item__img" alt="Slot preview">
                        <div class="item-text">
                            <h5 class="h5">Black Diamond</h5>
                            <p class="item-text__p">RushGameStudio</p>
                        </div>
                    </div></a>
                </div>
                <div class="catalog-banners d-flex d-flex-colum">
                    <div class="banners-top d-flex">
                        <div class="banners-item d-flex d-flex-colum">
                            <div class="item-text d-flex d-flex-colum">
                                <h5 class="h5">Dynamite Riches Megaways</h5>
                                <p>Miners revealed a gain of €46,672 for Sandra M.! You too, dynamite the reels of the Red Tiger Daily Jackpot machines</p>
                            </div>
                            <a href="#"><div class="item-btn d-flex d-flex-justify-center d-flex-align-center">Play now</div></a>
                        </div>
                        <div class="banners-item d-flex d-flex-colum">
                            <div class="item-text d-flex d-flex-colum">
                                <h5 class="h5">Gator Gold Deluxe Gigablox</h5>
                                <p>These swamps conceal many dangers but especially precious treasures. Will you be able to find them?</p>
                            </div>
                            <a href="#"><div class="item-btn d-flex d-flex-justify-center d-flex-align-center">Play now</div></a>
                        </div>
                    </div>
                    <div class="banner-bottom">
                        <div class="banner-item">
                            <img src="../assets/images/banner_promo.jpeg" alt="Banner promo" class="banner-item__img">
                            <div class="banner-item__info d-flex d-flex-justify-between d-flex-align-center">
                                <div class="item-text">
                                    <h5 class="h5">Our deals are not to be missed</h5>
                                    <p class="item-text__p">Discover a wide range of weekly promotions</p>
                                </div>
                                <a href="#"><div class="item-btn d-flex d-flex-justify-center d-flex-align-center">Read more</div></a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <p class="warn">* We don't offer opportunities to play for real money. Our games are free demo. All games were invented for entertainment purposes only and do not offer real money prizes.</p>
        </div>

        <ContactBlock />
        
        <img class="slot" src="../assets/images/image.png" alt="Slot">
    </div>
</template>

<style lang="scss">
@use "@/assets/breakpoints";

.games {
    width: 100%;
    padding-top: 54px;
    min-height: 1070px;
    grid-gap: 24px;
    position: relative;

    &-wrapper {

        width: 1039px;
        grid-gap: 24px;

        @include breakpoints.media-under-xl {

            max-width: 512px;
        }

        @include breakpoints.media-under-sm {

            max-width: 322px;
        }
    }

    &-title {

        grid-gap: 2px;

        

        .subtitle {

            @include breakpoints.media-under-xs {

                .subtitle-p {
                    max-width: 225px;
                }
            }
        }
    }

    &-catalog {

        width: 1039px;
        min-height: 336px;
        grid-gap: 16px;
        z-index: 5;


        @include breakpoints.media-under-xl {

            height: auto;
            max-width: 80%;
            justify-content: center;
            margin: 0 auto;
            flex-wrap: wrap;
        }

        .catalog-slots {
            display: grid;
            grid-gap: 16px;
            grid-template-columns: 160px 160px 160px;
            grid-template-rows: 160px 160px;

            @include breakpoints.media-under-sm {
                
                display: grid;
                grid-gap: 16px;
                grid-template-columns: 160px 160px !important;
                grid-template-rows: 160px 160px 160px !important;
            }

            .slots-item {

                .h5 {

                    white-space: nowrap;
                    overflow: hidden;
                }

                .slots-item__img {

                    width: 160px;
                    height: 120px;
                    border-radius: 16px;
                }

                .item-text__p {
                    font-size: 12px;
                    color: var(--white-transparent);
                }
            }

            .slots-item:hover .h5 {

                transition: 0.1s;
                color: var(--blue-link-text);
            }
        }

        .catalog-banners {

            grid-gap: 16px;

            .banners-top {
                
                grid-gap: 16px;

                @include breakpoints.media-under-sm {
                
                    flex-direction: column;
                    align-items: center;

                    .banners-item {
                        width: 336px !important;
                    }
                }

                .banners-item {

                    width: 248px;
                    height: 160px;
                    border-radius: 16px;
                    padding: 16px 12px;
                    grid-gap: 16px;

                    .item-text {
                        
                        grid-gap: 5px;

                        .h5 {
                            width: 150px !important;
                            min-height: 38px !important;
                        }

                        p {
                            max-width: 162px;
                            font-size: 10px;
                        }
                    }

                    a {
                        width: 68px;

                        .item-btn {
                            width: 68px;
                            height: 22px;
                            border-radius: 12px;
                            font-size: 10px;
                            color: var(--white);
                            background-color: var(--blue-link-text);
                        }
                    }
                }

                .banners-item:first-child {
                    background-image: url('../assets/images/games/DynamiteRichesMW_BigWin_385x190.jpeg');
                    background-size: cover;
                    background-position-x: center;
                }
                .banners-item:last-child {
                    background-image: url('../assets/images/games/GOTM_GatorGold_385x190.jpeg');
                    background-size: cover;
                }
            }

            .banner-bottom {
                
                .banner-item {

                    width: 512px;
                    height: 160px;

                    @include breakpoints.media-under-sm {

                        width: 336px !important;

                        .banner-item__img {
                            
                            width: 100%;
                            overflow: hidden;
                        }
                    }

                    .banner-item__img {

                        width: 100%;
                        height: 120px;
                        border-radius: 16px;
                    }

                    .banner-item__info {

                        .h5 {
                            width: 222px !important;
                        }

                        .item-text__p {
                            font-size: 12px;
                            color: var(--white-transparent);
                        }

                        .item-btn {
                            width: 81px;
                            height: 22px;
                            border-radius: 17px;
                            font-size: 10px;
                            color: var(--white);
                            background-color: var(--blue-link-text);
                        }
                    }
                }
            }
        }
    }

    .warn {
        font-size: 14px;
        max-width: 655px !important;
    }
}

.games::before {

    content: "";
    background-image: url('../src/assets/images/bg_contact.jpeg');
    background-size: cover;
    background-position-x: center;
    background-position-y: bottom;
    opacity: 0.5 !important;
    position: absolute;
    z-index: -1;
    top: 0px; left: 0; right: 0; bottom: 0;
    width: 100%;
    height: 100%;
}

.slot {

    position: absolute;
    bottom: 10px;
    right: 10%;
    z-index: 1;

    @include breakpoints.media-under-xl {

        display: none !important;
    }
}
</style>