<template>
  <v-navigation-drawer v-model="value" clipped fixed app>
    <v-list>
      <v-list-group
        v-for="(group, i) in groups"
        :key="i"
        active-class="white--text"
      >
        <template v-slot:activator>
          <v-list-item-title v-html="group.groupName" class="body-1" />
        </template>

        <v-list-item
          v-for="(item, j) in group.items"
          :key="j"
          active-class="white--text"
          :to="item.to"
        >
          <v-list-item-title
            v-html="item.title"
            class="body-2"
          ></v-list-item-title>
        </v-list-item>
      </v-list-group>
      <div style="height: 48px"></div>
      <div class="d-flex flex-column align-center">
        <v-btn color="success" class="mb-4">
          <nuxt-link to="/testing" class="text-decoration-none black--text"> Итоговое тестирование </nuxt-link>
        </v-btn>
        <v-btn color="success">
          <nuxt-link to="/practice" class="text-decoration-none black--text"> Практические задания </nuxt-link>
        </v-btn>
      </div>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: "NavigationDrawer",
  props: {
    value: { type: Boolean, default: false },
  },
  data() {
    return {
      groups: [
        {
          groupName: "Введение и </br>начало работы",
          items: [
            {
              title: "Введение",
              to: "/guide/1 introduction",
            },
            {
              title: "Ваше первое приложение",
              to: "/guide/2 newapp",
            },
            {
              title: "Маршрутизация",
              to: "/guide/3 route",
            },
            {
              title: "Развертывание",
              to: "/guide/4 razvr",
            },
            {
              title: "Настройка",
              to: "/guide/5 manage",
            },
          ],
        },
        {
          groupName: "Cli команды",
          items: [
            {
              title: "Обзор",
              to: "/guide/2.1 overwiev",
            },
            {
              title: "Аналитика использования",
              to: "/guide/2.2 usage",
            },
          ],
        },
      ],
    };
  },
};
</script>
