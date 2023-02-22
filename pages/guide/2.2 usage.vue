<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card>
            <div>
              <h2 class="mt-6">Сбор и просмотр аналитики использования </h2>
              <v-divider class="mb-6" />
              <p>Пользователи могут согласиться поделиться своими данными об использовании Angular CLI с Google Analytics, используя команду ng analytics CLI. Эти данные также передаются команде Angular и используются для улучшения пользовательского интерфейса.</p>
            <p>Сбор данных CLI analytics отключен по умолчанию и должен быть включен отдельными пользователями на уровне проекта. Это не может быть включено на уровне проекта для всех пользователей.</p>
            <p>Данные, собранные таким образом, можно просмотреть на сайте Google Analytics, но они не отображаются автоматически на сайте аналитики вашей собственной организации. Как администратор группы разработчиков Angular, вы можете настроить свой экземпляр Angular CLI таким образом, чтобы иметь возможность просматривать аналитические данные об использовании Angular CLI вашей собственной командой. Этот параметр конфигурации является отдельным от других аналитических данных об использовании, которыми ваши пользователи могут делиться с Google, и дополняет их.</p>
            </div>
          </div>

          <div>
            <h2 class="mt-6">Разрешить доступ к данным об использовании CLI</h2>
            <v-divider class="mb-6" />
            <p>
              Чтобы настроить доступ к данным об использовании CLI ваших собственных пользователей, используйте команду ng config для добавления ключа в ваш глобальный файл конфигурации рабочей области angular.json. Ключ находится в разделе cli.analyticsSharing на верхнем уровне файла, за пределами разделов проектов. Значением ключа является идентификатор отслеживания вашей организации, присвоенный Google Analytics. Этот идентификатор представляет собой строку, которая выглядит как UA-123456-12.</p>
            <p>Вы можете выбрать использование описательной строки в качестве значения ключа или присвоение случайного ключа при выполнении команды CLI. Например, следующая команда добавляет конфигурационный ключ с именем "отслеживание".</p>
            <p><div class="language-html line-numbers-mode">
              <pre
                class="language-html"
              ><span class="pln"> </span><span class="pun">--</span><span class="pln">global cli</span><span class="pun">.</span><span class="pln">analyticsSharing</span><span class="pun">.</span><span class="pln">tracking UA</span><span class="pun">-</span><span class="lit">123456</span><span class="pun">-</span><span class="lit">12</span>
              
</span>  
</span>
</code></pre>
            </div>
            <p>Чтобы отключить эту функцию, выполните следующую команду:</p>
            <p><div class="language-html line-numbers-mode">
              <pre
                class="language-html"
              ><span class="pln"> </span><span class="pln">ng </span><span class="pln">config</span><span class="pln"> </span><span class="pun">--</span><span class="pln">global </span><span class="pun">--</span><span class="pln">remove cli</span><span class="pun">.</span><span class="pln">analyticsSharing</span>
              
</span>  
</span>
</code></pre>
            </div>
            
          </div>

          <div>
            <h2 class="mt-6">Отслеживание каждого пользователя</h2>
            <v-divider class="mb-6" />
            <p>
              Вы можете добавить пользовательский идентификатор пользователя в глобальную конфигурацию, чтобы идентифицировать уникальное использование команд и флагов. Если этот пользователь включает CLI analytics для своего собственного проекта, ваш дисплей аналитики отслеживает и помечает их индивидуальное использование.</p>
            <p><div class="language-html line-numbers-mode">
              <pre
                class="language-html"
              ><span class="pln">ng </span><span class="pln">config</span><span class="pln"> </span><span class="pun">--</span><span class="pln">global cli</span><span class="pun">.</span><span class="pln">analyticsSharing</span><span class="pun">.</span><span class="pln">user SOME_USER_NAME</span>
              
</span>  
</span>
</code></pre>
            </div>
           <p>Чтобы сгенерировать новый случайный идентификатор пользователя, выполните следующую команду:</p>
         <p><div class="language-html line-numbers-mode">
              <pre
                class="language-html"
              ><span class="pln">ng </span><span class="pln">config</span><span class="pln"> </span><span class="pun">--</span><span class="pln">global cli</span><span class="pun">.</span><span class="pln">analyticsSharing</span><span class="pun">.</span><span class="pln">user </span><span class="str">""</span>
              
</span>  
</span>
</code></pre>
            </div>
            
          </div>

          

          <v-btn
            class="mt-6"
            color="success"
            nuxt
            to="/testing"
          >
            Пройти тест
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

