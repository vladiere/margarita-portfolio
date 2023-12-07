<style lang="sass" scoped>
.my-card
  width: 300px
</style>

<template>
  <q-page padding class="column flex flex-center q-pb-xl">

    <span class="text-h2 text-weight-bolder about-me q-mb-xl">MY <span class="text-green-6">WORK</span></span>

    <div :class="!Platform.is.mobile ? 'row jsutify-center q-gutter-x-lg' : 'column q-gutter-y-lg'">
      <q-card class="my-card">
        <img src="https://images.pexels.com/photos/3299/postit-scrabble-to-do.jpg?auto=compress&cs=tinysrgb&w=400">

        <q-card-section>
          <div class="text-h6">ToDo App with VUE and Firebase</div>
        </q-card-section>

        <q-card-actions class="q-pt-none">
          <q-btn flat icon="mdi-web" />
          <q-btn flat icon="mdi-github" />
        </q-card-actions>
      </q-card>

      <q-card class="my-card">
        <img src="https://images.pexels.com/photos/270408/pexels-photo-270408.jpeg?auto=compress&cs=tinysrgb&w=400">

        <q-card-section>
          <div class="text-h6">My Unique app</div>
        </q-card-section>

        <q-card-actions class="q-pt-none">
          <q-btn flat icon="mdi-web" />
          <q-btn flat icon="mdi-github" />
        </q-card-actions>
      </q-card>
    </div>

  </q-page>
</template>

<script setup>
import { defineComponent } from 'vue';
import { Platform } from 'quasar';

defineComponent({
  name: 'ServicePage'
});
</script>
