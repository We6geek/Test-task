<script setup>
import Preloader from '@/components/Preloader.vue';
import DashboardWrapper from '@/components/DashboradWrapper.vue';
import TitleBlock from '@/components/TitleBlock.vue';
import GamesBlock from '@/components/GamesBlock.vue';

</script>

<script>
export default {
  components: {
    Preloader
  },
  data() {
    return {
      loading: true
    };
  },

  mounted() {
    setTimeout(() => {
      this.loading = false;
    }, 2000);
  }
};
</script>

<template>
    <Preloader v-if="loading" />

    <DashboardWrapper v-else>

      <!-- блоки сюда -->
      <TitleBlock />
      <GamesBlock />
      <!-- блоки сюда -->

    </DashboardWrapper>
</template>

<style lang="scss">
@use "@/assets/main.scss";


</style>
