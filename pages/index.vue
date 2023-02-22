<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card>
        <v-sheet class="pa-4">
          <h1>Аннотация к курсу</h1>

          <div class="mt-6">
            <p>
              Целью изучения данного курса является получение базовых
              теоретических и практических навыков в фреймворке языка
              программирования JavaScript - Angular
            </p>
            <p class="mb-0">Задачи учебного курса:</p>
            <ul class="mb-4">
              <li>Изучить фреймворк Angular, его синтаксис</li>
              <li>
                Научиться разворачивать веб-приложение, написанное на Angular
              </li>
              <li>
                Понять устройство фреймворка изнутри для написания собственных
                программных интерфейсов
              </li>
              <li>
                На основе примеров изучить, как создавать различные элементры
                веб-страниц - от базовых компонентов до форм и целых страниц
              </li>
            </ul>
            <p class="mb-0">По завершении курса Вы приобретёте навыки:</p>
            <ul class="mb-4">
              <li>· Разворачивая проектов на Angular</li>
              <li>· Разработки собственных веб-приложений и страниц</li>
              <li>· Углублённого понимания устройства языка и его компонентов</li>
              <li>· Обработки потока данных на странице</li>
            </ul>
            <p>А также сможете применять полученные знания на практике.</p>
            <p class="mb-0">
              На данный момент курс содержит два основных раздела:
            </p>
            <ul class="mb-4">
              <li>
                Введение и начало работы - от введения до основ компонентов. На раздел
                выделяется 16 академических часов
              </li>
              <li>
                Сli команды - от их регистрации до передачи атрибутов
                и свойств. На раздел выделяется 2 академических часа
              </li>
            </ul>
            <h3 class="mb-4">Список рекомендуемых к изучению источников</h3>
            <div class="d-flex flex-column">
              <a
                href="https://angular.io/"
                class="text-decoration-none yellow--text"
                >Официальная документация Angular</a
              >
              <a
                href="https://angular-doc.ru/"
                class="text-decoration-none yellow--text"
                >Документация Angular на русском</a
              >
              <a
                href="https://metanit.com/web/angular2/?ysclid=leev48onfv787312717"
                class="text-decoration-none yellow--text"
                >Руководство по Angular 15</a
              >
              <a
                href="https://github.com/Angular-RU/angular-awesome-list?ysclid=leezy0fjnb42782418/"
                class="text-decoration-none yellow--text"
                >Github Angular на русском</a
              >
              <a
                href="https://itproger.com/course/angular"
                class="text-decoration-none yellow--text"
                >Уроки Angular</a
              >
            </div>
          </div>

          <v-btn class="mt-4" color="primary" nuxt to="/guide/1 introduction">
            Начать изучать курс
          </v-btn>
        </v-sheet>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>
