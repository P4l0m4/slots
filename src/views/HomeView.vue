<template>
  <div class="home">
    <h1 class="home__title">
      {{ msg }}
    </h1>
    <div class="home__actions">
      <PButton label="Plop" primary>
        <template #left>🐙</template>
        <template #right>🐙</template>
      </PButton>
      <PButton label="Hi" secondary><template v-slot:right>🦚</template></PButton>
      <PButton label="Bubu" tertiary><template v-slot:right>🦃</template></PButton>
    </div>
  </div>
</template>

<script>
import PButton from '@/components/PButton.vue'

export default {
  name: 'HomeView',
  components: {
    PButton,
  },
  data: vm => ({
    msg: vm.$t('home.title'),
  }),
}
</script>

<style lang="scss" scoped>
.home {
  display: flex;
  flex-flow: column wrap;
  align-content: center;
  justify-content: center;
  height: 100%;

  &__title {
    margin-top: 24px;
    margin-bottom: 1.5rem;
  }

  &__actions {
    display: flex;
    gap: 1rem;

    &__strong {
      color: black;
    }
  }
}
</style>
