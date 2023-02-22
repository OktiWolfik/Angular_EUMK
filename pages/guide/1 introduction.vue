<template>
   <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card>
        <v-sheet class="pa-4">
          <h1>Введение</h1>
          <hr class="my-3" />
          
          <div class="mt-6">
            <div>
              <h2>Документация по фреймворку Angular</h2>
              <v-divider class="mb-6" />
              <p>
                В документации по фреймворку Angular содержится основная информация 
                по использованию платформы и фреймворка Angular, включая разработку 
                первого приложения и оптимизацию сложного корпоративного программного 
                обеспечения. В уроках также есть примеры, что поможет Вам быстро приступить 
                к разработке приложений.
              </p>
            </div>

            <div>
              <h2 class="mt-6">Принятые допущения</h2>
              <v-divider class="mb-6" />
              <p>
                При разработке документации учитывался тот факт, что Вы 
                уже знакомы с HTML, CSS, <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Language_Overview">JavaScript</a> и с некоторыми инструментами 
                <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/JavaScript_technologies_overview">современных стандартов</a>, например классы и модули. Примеры кода 
                написаны на языке TypeScript. В большинстве случаев, код Angular 
                может быть написан на последней версии JavaScript, при этом типы 
                используются для внедрения зависимостей, а декораторы для отображения метаданных.
              </p>
              <p>
                На странице установки перечислено несколько вариантов как
                устанавливать Vue. Примечание: начинающим программистам не
                рекомендуем стартовать с <code>vue-cli</code>, особенно если ещё
                не знакомы с инструментами сборки на основе Node.js.
              </p>
            </div>
          </div>

          <v-btn
            class="mt-6"
            color="success"
            nuxt
            to="/guide/2 newapp"
          >
            Начало работы
          </v-btn>
        </v-sheet>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import SuccessAlert from "~/components/SuccessAlert.vue";

export default {
  name: "GuideIntroduction",
  components: { SuccessAlert },
};
</script>
