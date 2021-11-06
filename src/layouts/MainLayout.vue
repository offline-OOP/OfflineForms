<template>
  <q-layout view="lHh Lpr lFf">
    <q-header>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          OFFLINE. Аналитика и опросы
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
          Дополнительные ссылки
        </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksList = [
  {
    title: 'Разработка',
    caption: 'Всё, что касается программирования',
    icon: 'school',
    link: 'https://www.storybook.artoffline.ru/'
  },
  {
    title: 'Discord',
    caption: 'Discord сервер',
    icon: 'chat',
    link: 'https://discord.gg/b38Sk6qDKS'
  },
  {
    title: 'Twitter',
    caption: '@artoffline_news',
    icon: 'rss_feed',
    link: 'https://twitter.com/artoffline_news'
  },
  {
    title: 'Instagram',
    caption: '@artoffline.app',
    icon: 'photo_camera',
    link: 'https://www.instagram.com/artoffline.app/'
  },
  {
    title: 'Facebook',
    caption: '@artoffline',
    icon: 'group',
    link: 'https://www.facebook.com/groups/artoffline'
  },
  {
    title: 'VK',
    caption: '@artoffline',
    icon: 'groups',
    link: 'https://vk.com/artoffline'
  },
  {
    title: 'YouTube',
    caption: 'Канал OFFLINE',
    icon: 'video_library',
    link: 'https://www.youtube.com/channel/UCFKO_nkFNwOddBtd5Wjx3lg'
  },
  {
    title: 'TikTok',
    caption: '@artoffline',
    icon: 'timelapse',
    link: 'https://www.tiktok.com/@artoffline'
  },
  {
    title: 'Email',
    caption: 'semby@artoffline.ru',
    icon: 'contact_mail',
    link: 'mailto:semby@artoffline.ru'
  }
];

import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink
  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
