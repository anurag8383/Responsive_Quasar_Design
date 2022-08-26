<template>
  <q-layout view="lHh Lpr lFf">
    <q-resize-observer @resize="onResize"/>
    <q-header>
      <q-toolbar>
        <q-toolbar-title>
          <q-img class="imge" src="https://t3.ftcdn.net/jpg/04/43/10/12/360_F_443101282_x88vQ5SdTGNKxx36RelWJ7crqRk5trSE.jpg"
            style="width: 120px; border-radius: 30%; height: 70px; " />
        </q-toolbar-title>

        <div class="gt-sm">
          <q-btn outline rounded label="Home" class="q-mr-sm" />
          <q-btn outline rounded label="SignIn" class="q-mr-sm" />
          <q-btn outline rounded label="SignUp" class="q-mr-sm" />

        </div>
        <div class="lt-md">
          <q-btn flat dense round icon="menu" aria-label="Menu" @click="toggleLeftDrawer" />
        </div>
      </q-toolbar>
    </q-header>
    <q-drawer v-model="leftDrawerOpen" bordered content-class="bg-grey-2">
      <q-list>
        <q-item-label header>
          Essential Links
        </q-item-label>
        <EssentialLink v-for="link in essentialLinks" :key="link.title" v-bind="link" />
        <q-item clickable tag="a" target="_blank"
          href="https://www.youtube.com/watch?v=fN2-1V2YARQ&list=PLAl8os33KyOXvyPhuO1gHr6YVlTZXzKiS&index=3">
          <q-item-section avatar>
            <q-icon name="Home"></q-icon>
          </q-item-section>
          <q-item-section>
            <q-item-label>Home</q-item-label>
            <q-item-label caption>quasar.dev</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import EssentialLink from 'components/EssentialLink.vue'



export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink,
  },

  setup() {
    const leftDrawerOpen = ref(false)

    // return {
    //   essentialLinks: linksList,
    //   leftDrawerOpen,
    //   toggleLeftDrawer() {
    //     leftDrawerOpen.value = !leftDrawerOpen.value
    //   }
    // }
    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
<style scoped>
.imge{
  opacity: 0.6;
  border: none;
  height: 100vh;
  object-fit: cover;
  margin-top: 1%;
  margin-bottom: 1%;
}
/* .btn {
  font-family: "Trirong", serif;
} */
</style>
