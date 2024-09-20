<script setup>

</script>

<template>
    <div class="contact d-flex d-flex-colum">
        <div class="contact-title d-flex d-flex-colum">
            <h2 class="h2">Contact Us</h2>
            <p class="subtitle-p">If you have some questions, send us a message</p>
        </div>
        <div class="contact-form">
            <form class="form d-flex d-flex-colum" action="" method="post">
                <div class="form-inputs d-flex d-flex-colum">
                    <input class="input-text" type="text" placeholder="Firstname" required>
                    <input class="input-text" type="email" placeholder="Email Address" required>
                    <textarea class="input-text" placeholder="Your message here..." name="" id="" cols="30" rows="10"></textarea>
                </div>
                <div class="form-policy d-flex d-flex-align-center d-flex-justify-between">
                    <div class="policy-wrapper d-flex d-flex-align-center">
                        <input class="input-checkbox" type="checkbox" name="Policy" id="">
                        <label for="Policy">I Accept The <a href="#">Privacy Policy</a></label>
                    </div>
                    <button class="button" type="submit">Send</button>
                </div>
            </form>
        </div>
    </div>
</template>

<style lang="scss">
@use "@/assets/breakpoints";

    .contact {
        width: 1039px;
        margin-top: 50px;
        grid-gap: 25px;

        @include breakpoints.media-under-xl {

            align-items: start;
            max-width: 512px;
            grid-gap: 24px;
            height: auto;
        }

        @include breakpoints.media-under-md {

            width: 80%;
        }

        @include breakpoints.media-under-sm {

            width: 336px;
        }

        &-title {

            grid-gap: 2px;
        }

        &-form {

            .form {
                width: 400px;
                grid-gap: 20px;

                @include breakpoints.media-under-sm {

                    width: 336px;
                }

                .form-inputs {

                    grid-gap: 16px;

                    .input-text {
                        width: 100%;
                        height: 44px;
                        border-radius: 8px;
                        padding: 12px 14px;
                        font-size: 16px;
                        color: var(--blue-text);
                    }

                    .input-text:last-child {
                        height: 128px;
                        border-radius: 8px;
                        padding: 12px 14px;
                        font-size: 16px;
                        color: var(--blue-text);
                    }
                }

                .form-policy {

                    @include breakpoints.media-under-sm {

                        width: 336px;
                    }

                    .policy-wrapper {

                        grid-gap: 5px;

                        label {

                            font-size: 14px;
                            line-height: 20px;
                            color: var(--white);

                                a {

                                    text-decoration: solid underline;
                                    color: var(--white);
                                }
                            }
                    }
                }
            }
            
        }
    }
</style>