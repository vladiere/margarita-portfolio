<template>
  <q-page padding class="column flex flex-center q-pb-xl">

    <span class="text-h2 text-weight-bolder about-me q-mb-xl">GET IN <span class="text-green-6">TOUCH</span></span>

    <div :class="!Platform.is.mobile ? 'row q-gutter-x-lg q-pa-md' : 'column q-gutter-y-lg q-pa-md'">
      <div class="col column q-gutter-y-lg">
        <span class="text-h5 text-weight-regular text-grey-8">DONT'T BE SHY!</span>
        <span class="text-subtitle1 text-weight-regular text-grey-7">Feel free to get in touch with me. I am always open to discussing new projects, creative ideas or opportunities to be part of your visions.</span>

        <div class="row q-gutter-x-md items-center">
          <q-icon name="mdi-email-open" color="green-6" size="3em" />
          <div class="column">
            <span class="text-subtitle1 text-grey-7 text-weight-regular">MAIL ME</span>
            <span class="text-subtitle2 text-weight-regular text-grey-9">ma.margaritaybanez@gmail.com</span>
          </div>
        </div>

        <div class="row q-gutter-x-md items-center">
          <q-icon name="mdi-phone" color="green-6" size="3em" />
          <div class="column">
            <span class="text-subtitle1 text-grey-7 text-weight-regular">CALL ME</span>
            <span class="text-subtitle2 text-weight-regular text-grey-9">(+639)969 - 1125 - 876</span>
          </div>
        </div>

      </div>

      <div class="column q-gutter-y-md">
        <div :class="!Platform.is.mobile ? 'row q-gutter-x-md' : 'column q-gutter-y-lg'">
          <q-input outlined rounded v-model="form.name" placeholder="YOUR NAME" />
          <q-input outlined rounded v-model="form.email" placeholder="YOUR EMAIL" />
          <q-input outlined rounded v-model="form.subject" placeholder="YOUR SUBJECT" />
        </div>
        <q-input outlined rounded v-model="form.message" type="textarea" placeholder="YOU MESSAGE" />
        <q-btn outline rounded style="color: green" label="send message" icon="telegram" class="self-start" size="md"/>
      </div>
    </div>

  </q-page>
</template>

<script setup>
import { defineComponent, ref } from 'vue';
import { Platform } from 'quasar';

defineComponent({
  name: 'ContactPage'
});

const form = ref({
  name: '',
  email: '',
  subject: '',
  message: ''
})
</script>
