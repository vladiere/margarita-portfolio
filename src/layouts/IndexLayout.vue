<template>
  <q-layout view="hhh lpR fFf">

    <q-header v-if="Platform.is.mobile" class="bg-transparent text-green-6">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="toggleRightDrawer" />
      </q-toolbar>
    </q-header>

    <q-drawer
      show-if-above
      v-model="rightDrawerOpen"
      side="right"

      :width="!Platform.is.mobile ? 90 : 200"
      :breakpoint="500"

      :class="!Platform.is.mobile ? 'column justify-center items-center q-gutter-y-xl bg-transparent' : 'window-height bg-green-6 column justify-center q-gutter-y-xl'"
    >
      <!-- drawer content -->
      <q-btn round :flat="Platform.is.mobile" :text-color="routeName === 'home' ? 'grey-1' : 'grey-7'" :color="routeName === 'home' ? 'green-6' : 'grey-5'" icon="mdi-home" :label="Platform.is.mobile ? 'Home' : ''" size="lg" padding="10px" to="/">
          <q-tooltip class="bg-green-6 text-white" anchor="center left" self="center middle">
            Home
          </q-tooltip>
        </q-btn>
      <q-btn round :flat="Platform.is.mobile" :text-color="routeName === 'about' ? 'grey-1' : 'grey-7'" :color="routeName === 'about' ? 'green-6' : 'grey-5'" icon="mdi-account" :label="Platform.is.mobile ? 'About' : ''"  size="lg" padding="10px" to="about">
          <q-tooltip class="bg-green-6 text-white" anchor="center left" self="center middle">
            About
          </q-tooltip>
        </q-btn>
      <q-btn round :flat="Platform.is.mobile" :text-color="routeName === 'service' ? 'grey-1' : 'grey-7'" :color="routeName === 'service' ? 'green-6' : 'grey-5'" icon="mdi-briefcase-variant" :label="Platform.is.mobile ? 'Service' : ''" size="lg"  padding="10px" to="service">
          <q-tooltip class="bg-green-6 text-white" anchor="center left" self="center middle">
            Service
          </q-tooltip>
        </q-btn>
        <q-btn round :flat="Platform.is.mobile" :text-color="routeName === 'contact' ? 'grey-1' : 'grey-7'" :color="routeName === 'contact' ? 'green-6' : 'grey-5'" icon="mdi-email-open" :label="Platform.is.mobile ? 'Contact' : ''" size="lg"  padding="10px" to="contact">
          <q-tooltip class="bg-green-6 text-white" anchor="center left" self="center middle">
            Contact
          </q-tooltip>
        </q-btn>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script setup>
import { ref, watch, onMounted } from 'vue';
import { Platform } from 'quasar';
import { useRouter } from 'vue-router';

const rightDrawerOpen = ref(false);
const miniState = ref(false);
const router = useRouter()
const routeName = ref('home');

const toggleRightDrawer = () => {
   rightDrawerOpen.value = !rightDrawerOpen.value
}

onMounted(() => {
  routeName.value = router.currentRoute.value.name;
})

watch(() => router.currentRoute.value.name, () => {
  routeName.value = router.currentRoute.value.name;
});
</script>
