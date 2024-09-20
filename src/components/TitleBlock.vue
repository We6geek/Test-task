<script setup>

</script>

<template>
    <div class="title d-flex d-flex-colum d-flex-align-center d-flex-justify-between">
        <div class="title-info d-flex d-flex-colum d-flex-align-center">
            <h1 class="h1">AWESOME HTML5 GAMES - NO MONEY!</h1>
            <h3 class="h3">Your Perfect Place To Get Some Fun And Excitement</h3>
            <div class="container-buttons d-flex">
                <a href="#"><button class="border-button" type="button">Log In</button></a>
                <a href="#"><button class="button" type="button">Play</button></a>
            </div>
        </div>
        <div class="title-form d-flex d-flex-colum">
            <div class="form-text d-flex d-flex-align-end d-flex-justify-between">
                <h4 class="h4">CREATE A FREE ACCOUNT NOW</h4>
                <div class="info-icons d-flex">
                    <span class="d-flex d-flex-align-center">
                        <img src="../assets/images/icons/ever.svg" alt="ico">
                        <p>1000+ Games available</p>
                    </span>
                    <span class="d-flex d-flex-align-center">
                        <img src="../assets/images/icons/games.svg" alt="ico">
                        <p>New game Every week</p>
                    </span>
                    <span class="d-flex d-flex-align-center">
                        <img src="../assets/images/icons/slot.svg" alt="ico">
                        <p>Support our users 24/7</p>
                    </span>
                </div>
            </div> 
            <div class="form-wrapper d-flex d-flex-align-center d-flex-justify-center">
                <form class="form d-flex d-flex-colum" action="" method="post">
                    <div class="form-inputs d-flex">
                        <input class="input-text" type="text" placeholder="Firstname" required>
                        <input class="input-text" type="text" placeholder="Lastname" required>
                        <input class="input-text" type="text" placeholder="Email Address" required>
                        <button class="button" type="submit">Join Now</button>
                    </div>
                    <div class="form-policy d-flex d-flex-align-center d-flex-justify-start">
                        <input class="input-checkbox" type="checkbox" name="Policy" id="">
                        <label for="Policy">I Accept The <a href="#">Privacy Policy</a></label>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
@use "@/assets/breakpoints";

.title {
    width: 100%;
    height: 593px;
    padding-top: 125px;
    background: url('../src/assets/images/bg_hero.png');
    background-size: cover;
    overflow: hidden;
    background-position-x: center;
    background-position-y: -250px;

    @include breakpoints.media-under-lg {

        height: auto;
        grid-gap: 60px;
    }

    &-info {
        grid-gap: 6px;

        .h1 {
            max-width: 605px;
            letter-spacing: 1px;
        }

        .h3 {
            max-width: 389px;
        }

        @include breakpoints.media-under-xs {

            .h3 {
                max-width: 260px;
            }
        }

        @include breakpoints.media-under-md {

            .h1 {
                max-width: 85%;
                font-size: 38px;
            }

            .h3 {
                font-size: 18px;
            }
        }
    }

    .container-buttons {
        grid-gap: 16px;
        margin-top: 24px;

        button {
            width: 160px;
            height: 44px;
        }

        @include breakpoints.media-under-md {

            button {
                width: 100px;
            }
        }
    }

    &-form {
        width: 864px;
        height: 150px;
        background: linear-gradient(80deg, rgba(79,89,124,0.4) 0%, rgba(123,135,175,0.4) 50%, rgba(63,72,105,0.4) 100%);
        backdrop-filter: blur(10px);
        border-radius: 16px;
        padding: 12px 16px 20px 16px;
        grid-gap: 12px;
        border: 1px solid #3A4054;

        @include breakpoints.media-under-lg {

            max-width: 600px;
            grid-gap: 24px;
            height: auto;
        }

        @include breakpoints.media-under-md {

            width: 80%;
        }

        @include breakpoints.media-under-xs {

            width: 336px;
        }

        .form-text {

            @include breakpoints.media-under-lg {

                grid-gap: 16px;
                flex-wrap: wrap;
                align-items: center;
                flex-direction: column !important;
            }
        }

        .info-icons {
            grid-gap: 24px;

            @include breakpoints.media-under-lg {

                flex-wrap: wrap;
                justify-content: center;
                grid-gap: 12px;
            }

            span {
                grid-gap: 6px;

                img {
                    width: 36px;
                    height: 36px;
                }
                
                p {
                    color: var(--white);
                    font-size: 12px;
                }
            }

            span:first-child > p {
                width: 74px !important;
            }
            span:nth-child(2) > p {
                width: 63px;
            }
            span:last-child > p {
                width: 66px;
            }
        }

        &-wrapper {
            width: 100%;
            height: 100%;

            @include breakpoints.media-under-lg {  

                margin: 0 auto !important;                
            }
        }

        .form {
            grid-gap: 12px;

            &-inputs {
                grid-gap: 16px;

                input {
                    padding-left: 14px;
                    font-size: 16px;
                    color: var(--blue-text);
                    width: 202px;
                }

                input:nth-child(3) {
                    width: 220px;
                }

                button {
                    width: 160px;
                    height: 44px;
                    box-shadow: 0 4px 16px 0 rgba(138, 97, 255, 0.6);
                }

                @include breakpoints.media-under-lg {
                    justify-content: center;
                    width: 350px;
                    margin: 0 auto;

                    input,
                    input:nth-child(3) {
                        
                        width: 100%;
                        height: 44px;
                    }

                    button {
                        width: 100%;
                        height: 44px;
                    }
                }

                @include breakpoints.media-under-md {

                    input,
                    button,
                    input:nth-child(3) {
                        width: 100%;
                        height: 44px;
                    }
                }

                @include breakpoints.media-under-xs {

                    width: 100%;
                }
            }

            &-policy {
                grid-gap: 8px;

                input,
                .input-checkbox {
                    width: 14px;
                    height: 14px;
                }

                label {
                    font-style: 14px;
                    color: var(--white);

                    a {
                        text-decoration: solid underline;
                        color: var(--white);
                    }
                }

                @include breakpoints.media-under-lg {

                    width: 100%;
                    justify-content: start;
                    align-items: start;
                    margin: 0 auto;
                }
            }

            @include breakpoints.media-under-lg {

                &-inputs {
                    flex-wrap: wrap;
                }
            }
        }
    }
}
</style>
