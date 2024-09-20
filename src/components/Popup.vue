<template>
    <div>
      <div v-if="isPopupActive" class="overlay" @click.self="closePopup"></div>
      
      <div v-if="isPopupActive" class="popup">
        <div class="popup-content d-flex d-flex-colum d-flex-justify-center d-flex-align-center">
            <h2 class="h2">Registration</h2>
          <button class="popup-close" @click="closePopup">✕</button>
          <form class="form d-flex d-flex-colum" action="" method="post">
            <div class="form-inputs d-flex d-flex-colum d-flex-align-center">
                <input class="input-text" type="text" placeholder="Login" required>
                <input class="input-text" type="email" placeholder="Email Address" required>
                <input class="input-text" type="password" placeholder="Password" required>
                <input class="input-text" type="password" placeholder="Confirm Password" required></input>
            </div>
            <div class="form-policy d-flex d-flex-align-center d-flex-justify-between">
                <div class="policy-wrapper d-flex d-flex-align-center">
                    <input class="input-checkbox" type="checkbox" name="Policy" id="">
                    <label class="label-policy" for="Policy">I Accept The <a href="#">Privacy Policy</a></label>
                </div>
                <button class="button" type="submit">Sing up</button>
            </div>
          </form>
        </div>
      </div>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        isPopupActive: false
      };
    },
    methods: {
      openPopup() {
        this.isPopupActive = true;
      },
      closePopup() {
        this.isPopupActive = false;
      }
    }
  };
</script>
  
<style lang="scss">
@use "@/assets/breakpoints";

  .popup {
    position: absolute;
    bottom: calc(-50vh - 300px);
    left: 50%;
    transform: translate(-50%, -50%);
    width: 550px;
    height: auto;
    padding: 50px;
    background: var(--blue-main);
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.2);
    z-index: 100;
    border-radius: 10px;

    @include breakpoints.media-under-md {
        width: 60%;
        height: 375px;
        padding: 30px 5px;

        .input-text {
            width: 100% !important;
        }

        .popup-close {

            top: -15px;
            right: 5px;
        }
    }

    @include breakpoints.media-under-sm {
        width: 80%;
        height: 375px;
        padding: 30px 5px;

        .input-text {
            width: 100% !important;
        }

        .popup-close {

            top: -15px;
            right: 5px;
        }
    }
  }
  
  .popup-content {
    position: relative;
    margin: 0 auto;
    width: 100%;
    height: 100%;
    grid-gap: 15px;

    form {
        width: 80%;
        height: 80%;
        grid-gap: 15px;

        .form-inputs {
            grid-gap: 10px;

            .input-text {
                padding-left: 14px;
                font-size: 16px;
                color: var(--blue-text);
                width: 90%;
                height: 44px !important;
            }

            .input-text:last-child {
                
            }
        }

        .form-policy {

            .input-checkbox {

                width: 14px;
                height: 14px;
                margin-right: 8px;
            }

            .label-policy, a {
                color: var(--white) !important;
            }

            a {
                text-decoration: solid underline;
            }
        }
    }
  }
  
  .popup-close {
    position: absolute;
    top: -30px;
    right: -30px;
    background: none;
    border: none;
    font-size: 20px;
    cursor: pointer;
    color: #ffffff;
  }
  
  .overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 50;
  }
</style>
  