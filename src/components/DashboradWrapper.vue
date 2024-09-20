<script setup>
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";

</script>

<template>
  <div class="dashboard-wrapper">
    <div class="dashboard-wrapper__container">
      <Header />
      <div class="dashboard-wrapper__content">
        <slot></slot>
      </div>
      <Footer />
    </div>
  </div>
</template>

<style lang="scss">
@use "@/assets/breakpoints";

.dashboard-wrapper {
  &__container {
    min-width: 1400px;
    max-width: 100%;
    margin: 0 auto;
  }

  &__content {
    flex: 1 1 auto;
    display: flex;
    flex-direction: column;
  }

  @include breakpoints.media-under-xxl {
    &__container {
      min-width: unset;
      max-width: 100%;
      min-height: 72px;
    }

    &__content {
    }
  }

  @include breakpoints.media-under-lg{
    &__content {
      flex-direction: column;
    }
  }
}
</style>
