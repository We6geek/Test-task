<script>
    export default {
    data() {
        return {
        currentYear: new Date().getFullYear()
        };
    }
    };
</script>

<template>
    <footer>
        <div class="footer d-flex d-flex-colum d-flex-justify-center d-flex-align-center">
            <div class="footer-content d-flex d-flex-colum d-flex-align-center">
                <div class="content-links d-flex">
                    <a href="#"><p>Disclaimer</p></a>
                    <span><p>|</p></span>
                    <a href="#"><p>Privacy Policy</p></a>
                    <span><p>|</p></span>
                    <a href="#"><p>Terms of Conditions</p></a>
                </div>
                <p class="content-p">This site does not provide any form of online gambling and delivers information for entertainment and research purposes only. The games listed by Topwinningslots are intended for adult audience entertainment (underage visitors are restricted) and do not offer real money or prizes. Practicing online free games does not imply future success at 'real money' gambling.</p>
            </div>
            <div class="hr"></div>
            <div class="footer-info d-flex d-flex-justify-between d-flex-align-center">
                <div class="info-copyrights">
                    <p>{{ currentYear }} | © Lorem Inc. All Rights Reserved</p>
                </div>
                <div class="info-contacts d-flex">
                    <a href="#"><span class="icon-fa-brands_twitter"></span></a>
                    <a href="#"><span class="icon-fa-brands_facebook-f"></span></a>
                    <a href="#"><span class="icon-fa6-brands_instagram"></span></a>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
@use "@/assets/breakpoints";

    .footer {

        max-width: 1040px;
        margin: 0 auto;
        grid-gap: 23px;
        padding: 23px 0;

        @include breakpoints.media-under-xl {

            max-width: 864px;
        }

        @include breakpoints.media-under-lg {

            max-width: 80%;
            padding: 46px 0;

            .content-p {
                font-size: 10px;
            }
        }

        &-content {

            width: 100%;
            grid-gap: 15px;

            .content-links {
                grid-gap: 10px;

                p {
                    font-weight: 600;
                    transition: 0.1s;
                }

                p:hover {
                    color: var(--blue-link-text);
                }

                @include breakpoints.media-under-xs {

                    grid-gap: 5px;
                    font-size: 14px;
                }

                
            }

            .content-p {
                font-size: 14px;
                color: var(--white-transparent);
                text-align: center;

                @include breakpoints.media-under-md {

                    font-size: 12px;
                }
            }
        }

        .hr {

            width: 100%;
            height: 1px;
            background-color: var(--white);
            opacity: 0.1;
        }

        .footer-info {

            width: 100%;

            .info-copyrights {

                p {
                    font-size: 14px;

                    span {
                        font-weight: 600;
                    }
                }
            }

            .info-contacts {
                gap: 12px;

                span {
                    font-size: 16px;
                }
            }
        }

    }
</style>
