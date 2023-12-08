<template>
  <q-page padding class="column flex flex-center q-pb-xl">

    <span class="text-h2 text-weight-bolder about-me q-mb-xl">ABOUT <span class="text-green-6">ME</span></span>

    <div class="row q-gutter-x-xl">

      <div class="col column q-gutter-y-lg">
        <span class="text-h4 text-weight-bold text-grey-9">Personal Infos</span>

        <div class="row q-gutter-x-lg">

          <div class="column q-gutter-y-md">
            <div class="row q-gutter-x-lg">
              <span class="text-subtitle1 text-weight-light text-grey-7">First Name:</span>
              <span class="text-subtitle1 text-weight-bold text-grey-8">Margarita</span>
            </div>
            <div class="row q-gutter-x-lg">
              <span class="text-subtitle1 text-weight-light text-grey-7">Last Name:</span>
              <span class="text-subtitle1 text-weight-bold text-grey-8">Ybanez</span>
            </div>
            <div class="row q-gutter-x-lg">
              <span class="text-subtitle1 text-weight-light text-grey-7">Age:</span>
              <span class="text-subtitle1 text-weight-bold text-grey-8">29</span>
            </div>
            <div class="row q-gutter-x-lg">
              <span class="text-subtitle1 text-weight-light text-grey-7">Nationality:</span>
              <span class="text-subtitle1 text-weight-bold text-grey-8">Filipino</span>
            </div>
          </div>

          <div class="column q-gutter-y-md">
            <div class="row q-gutter-x-lg">
              <span class="text-subtitle1 text-weight-light text-grey-7">Address:</span>
              <span class="text-subtitle1 text-weight-bold text-grey-8">Andalucia Crest, Gabi, Cordova, Cebu</span>
            </div>
            <div class="row q-gutter-x-lg">
              <span class="text-subtitle1 text-weight-light text-grey-7">Phone:</span>
              <span class="text-subtitle1 text-weight-bold text-grey-8">(+639)969 - 1125 - 876</span>
            </div>
            <div class="row q-gutter-x-lg">
              <span class="text-subtitle1 text-weight-light text-grey-7">Email:</span>
              <span class="text-subtitle1 text-weight-bold text-grey-8">ma.margaritaybanex@gmail.com</span>
            </div>
            <div class="row q-gutter-x-lg">
              <span class="text-subtitle1 text-weight-light text-grey-7">Languages:</span>
              <span class="text-subtitle1 text-weight-bold text-grey-8">English, Cebuano, Tagalog</span>
            </div>
          </div>

        </div>
      </div>

      <iframe class="shadow-3" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3925.9518497973977!2d123.96159127402822!3d10.265463468412683!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x33a99a71f8aed98d%3A0xb8a30803d51c63c1!2sAndalucia%20Crest!5e0!3m2!1sen!2sph!4v1701947660072!5m2!1sen!2sph" :width="Platform.is.mobile ? '100%' : '485'" height="270" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>

  </q-page>
</template>

<script setup>
import { defineComponent } from 'vue';
import { Platform } from 'quasar';

defineComponent({
  name: 'AboutPage'
})
</script>
