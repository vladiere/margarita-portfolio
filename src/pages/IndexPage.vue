<style lang="sass" scoped>
.picture
  width: 100%
  height: 90vh
  border-radius: 30px
</style>

<template>
  <q-page padding class="flex flex-center q-pb-xl">
    <div :class="!Platform.is.mobile ? 'row q-gutter-x-xl items-center' : 'column q-gutter-y-lg items-center justify-center'">
      <div :class="!Platform.is.mobile ? 'col-4 q-mr-xl' : 'col q-pa-md'">
        <img :src="Picture" class="picture" />
      </div>
      <div class="col column q-gutter-y-md">
        <div class="column">
          <span class="text-h3 text-weight-bolder text-green-6 text-uppercase">Margarita Ybanez.</span>
          <span class="text-h3 text-weight-bolder text-grey-7 text-uppercase">Web developer</span>
          <span class="text-h6 text-weight-light text-grey-7 q-mt-xl">I'm Margarita Ybanez, a skilled web designer and front-end developer based in Tunisia. Committed to creating intuitive and visually appealing digital experiences, I bring passion and precision to every project, aiming to elevate online interactions and user satisfaction.</span>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import { defineComponent } from 'vue';
import { Platform } from 'quasar';
import Picture from 'src/assets/picture.jpg';

defineComponent({
  name: 'IndexPage'
})
</script>
