<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card>
            <div>
              <h2 class="mt-6">Настройка рабочего окружения</h2>
              <v-divider class="mb-6" />
              <p>Этот урок посвящен настройке среды программирования для фреймворка Angular с помощью инструмента Angular CLI. Описываются исходные параметры среды, установка CLI, создание начального рабочего пространства и стартового приложения, а также локальный запуск приложения для проверки настроек.</p>
              <SuccessAlert>
                ЗНАКОМИМСЯ С ANGULAR<br>
                Если раньше Вы не работали с Angular, ознакомьтесь с Руководством "С чего начать". С этим руководством вы быстро научитесь основам работы с Angular на примере создания простого Интернет-магазина. Здесь применяется StackBlitz - онлайн среда программирования, поэтому нет необходимости настраивать собственную локальную среду, пока Вы не будете готовы.
              </SuccessAlert>
            </div>
          </div>

          <div>
            <h2 class="mt-6">Предварительные требования</h2>
            <v-divider class="mb-6" />
            <p>
              До начала работы удостоверьтесь, что Ваша среда разработки содержит Node.js и диспетчер пакетов npm.
            </p>
            <p>NODE.JS<br>
            Для Angular требуется Node.js версии 10.9.0 или более поздней.<br>
            · Чтобы проверить Вашу версия Node.js, запустите команду node -v в окне терминала/консоли.<br>
            · Для установки Node.js перейдите на сайт nodejs.org.</p>
            <p>ДИСПЕТЧЕР ПАКЕТОВ NPM<br>
            Angular, Angular CLI и приложения на Angular, в зависимости от возможностей и функциональности, обеспечиваются библиотеками, известными как пакеты npm. Для загрузки и установки пакетов должен быть установлен диспетчер пакетов npm.</p>
          <p>В этом уроке используется консольный клиент npm, установленный с Node.js по умолчанию.</p>
          <p>Чтобы проверить, установлен ли npm, выполните команду npm -v в окне терминала/консоли.</p>
          </div>

          <div>
            <h2 class="mt-6">Шаг 1: установите Angular CLI</h2>
            <v-divider class="mb-6" />
            <p>
              Angular CLI используется для создания проектов, приложений, библиотек, и для выполнения других задач, например, тестирование, работа с пакетами и развертывание.
            </p>
            <p>Установите Angular CLI глобально.</p>
            <p>Для установки CLI используйте npm, откройте окно терминала/консоли и введите следующую команду:</p>
            <p><div class="language-html line-numbers-mode">
              <pre
                class="language-html"
              ><span class="pln">npm install </span><span class="pun">-</span><span class="pln">g </span><span class="lit">@angular</span><span class="pun">/</span><span class="pln">cli</span>
              
</span>  
</span>
</code></pre>
            </div>
           
         
          </div>

          <div>
            <h2 class="mt-6">Шаг 2: Создание рабочего пространства и стартового приложения</h2>
            <v-divider class="mb-6" />
            <p>Вы разрабатываете приложения в Angular workspace.</p>
            <p>Чтобы создать новое рабочее пространство и стартовое приложение,</p>
            <p>1. в командной строке запустите команду ng new и введите имя my-app:</p>
            <p><div class="language-html line-numbers-mode">
              <pre
                class="language-html"
              ><span class="pln">ng new my</span><span class="pun">-</span><span class="pln">app</span>
              
</span>  
</span>
</code></pre>
            </div>
            <p>2. Команда ng new подскажет, какую функциональность можно включить в стартовое приложение. Примите настройки по умолчанию, нажимая Enter.</p>
            <p>Angular CLI устанавливает необходимые пакеты Angular npm и другие зависимости, что может занять несколько минут.</p>
            <p>CLI создаст новое рабочее пространство и простое, готовое к использованию стартовое приложение.</p>
            
          </div>

          <div>
            <h2 class="mt-6">Шаг 3: Запустите приложение</h2>
            <v-divider class="mb-6" />
            <p>
              Angular CLI включает сервер, поэтому Вы легко можете создать и запустить свое приложение локально.
            </p>
            <p>1. Перейдите в папку рабочего пространства (my-app).</p>
            <p>2. Запустите сервер - в командной строке введите команду ng serve с опцией --open.</p>
            <p><div class="language-html line-numbers-mode">
              <pre
                class="language-html"
              ><span class="pln">cd my</span><span class="pun">-</span><span class="pln">app
ng serve </span><span class="pun">--</span><span class="pln">open</span>
              
</span>  
</span>
</code></pre>
            </div>
            <p>Команда ng serve запускает сервер, отслеживает файлы и пересобирает приложение при внесении изменений.</p>
            <p>Опция --open (или просто -o) автоматически откроет браузер на странице http://localhost:4200/.</p>
            <p>Появится приветственное сообщение:</p>
            <div class="d-flex justify-center">
              <v-img
                class="mb-4"
                max-width="297"
                height="347"
                src="https://angular-doc.ru/generated/images/guide/setup-local/app-works.png"
              />
            </div>
            
          </div>

          

          <v-btn
            class="mt-6"
            color="success"
            nuxt
            to="/guide/2.1 overwiev"
          >
            Слудующий раздел
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

