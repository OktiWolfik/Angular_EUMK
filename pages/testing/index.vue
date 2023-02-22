<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card>
        <v-sheet class="pa-4">
          <h1>Итоговое тестирование</h1>
          <hr class="my-3" />

          <v-form class="mt-6">
            <div class="mb-16">
              <h3>1. Что такое Angular?</h3>
              <v-checkbox
                hide-details
                v-model="first"
                label="Angular.JS — это фреймворк для работы с JavaScript"
                :value="1"
              />
              <v-checkbox
                hide-details
                v-model="first"
                label="Angular.JS — это программа для создания одностраничных приложений"
                :value="2"
              />
              <v-checkbox
                hide-details
                v-model="first"
                label="Angular.JS — это мобильное приложение"
                :value="3"
              />
            </div>

            <div class="mb-16">
              <h3>
                2. Для чего используется Angular?
              </h3>
              <v-radio-group v-model="second">
                <v-radio label="Смотреть видеоконтент" :value="1" />
                <v-radio label="Вычислять математические операции" :value="2" />
                <v-radio label="Создание одностраничных приложений" :value="3" />
                <v-radio label="Позволяет написать вирус" :value="4" />
              </v-radio-group>
            </div>

            <div class="mb-16">
              <h3>3. Укажите правильные утверждения по поводу директив в Angular 8</h3>
              <v-checkbox
                hide-details
                v-model="third"
                label="директива – это обычный класс, написанный на typescript, к которому применяется декоратор Directive"
                :value="1"
              />
              <v-checkbox
                hide-details
                v-model="third"
                label="ngSwitch – это атрибутивная директива"
                :value="2"
              />
              <v-checkbox
                hide-details
                v-model="third"
                :label="` директивы предназначены для изменения структуры DOM-дерева`"
                :value="3"
              />
              <v-checkbox
                hide-details
                v-model="third"
                :label="`директивы предназначены для изменения внешнего вида или поведения по-умолчанию элемента DOM-дерева`"
                :value="4"
              />
              <v-checkbox
                hide-details
                v-model="third"
                :label="` ngFor – это структурная директива`"
                :value="5"
              />
              <v-checkbox
                hide-details
                v-model="third"
                label="директивы предназначены для форматирования данных в таблице CSS"
                :value="6"
              />
              <v-checkbox
                hide-details
                v-model="third"
                :label="`ngClass – это структурная директива`"
                :value="7"
              />
            </div>

            <div class="mb-16">
              <h3>4. Директива в Angular может содержать:</h3>
              <v-checkbox
                hide-details
                v-model="fourth"
                :label="`всегда только один Input и один selector;`"
                :value="1"
              />
              <v-checkbox
                hide-details
                v-model="fourth"
                :label="`несколько Input’ов и один selector;`"
                :value="2"
              />
              <v-checkbox
                hide-details
                v-model="fourth"
                :label="`несколько селекторов, перечисленных через запятую;`"
                :value="3"
              />
              <v-checkbox
                hide-details
                v-model="fourth"
                :label="`в селекторе элемент input c атрибутами как целевой элемент HTML`"
                :value="4"
              />
            </div>

            <div class="mb-16">
              <h3>5. В чем разница между AngularJS и Angular?</h3>
              <v-radio-group v-model="fifth">
                <v-radio label="Первый библиотека, второй - фреймворк" :value="1" />
                <v-radio label="Первый на JavaScript, второй - на Python" :value="2" />
                <v-radio label="Первый является фреймворком, а второй то же самое, но с многими преимуществами" :value="3" />
              </v-radio-group>
            </div>

            <div class="mb-16">
              <h3>6. Укажите правильные утверждения, касающиеся привязки данных в Angular:</h3>
              <v-checkbox
                hide-details
                v-model="sixth"
                :label="`в Angular существует четыре односторонние привязки данных;`"
                :value="1"
              />
              <v-checkbox
                hide-details
                v-model="sixth"
                :label="` в Angular существует две двухсторонних привязки данных;`"
                :value="2"
              />
              <v-checkbox
                hide-details
                v-model="sixth"
                :label="`в Angular существует три односторонних привязки данных;`"
                :value="3"
              />
              <v-checkbox
                hide-details
                v-model="sixth"
                :label="` в Angular существует одна двусторонняя привязка данных;`"
                :value="4"
              />
              <v-checkbox
                hide-details
                v-model="sixth"
                :label="`в Angular существует три двухсторонних привязки данных`"
                :value="5"
              />
            </div>

            <div class="mb-16">
              <h3>
                7. Декоратор HostListener применяется в случаях, если:
              </h3>
              <v-radio-group v-model="seventh">
                <v-radio label="необходимо связать события DOM и методы директивы для изменения стандартного поведения DOM-элемента при возникновении пользовательского события;" :value="1" />
                <v-radio label="необходимо связать свойство класса со свойством DOM-элемента, к которому применяется директива для изменения стандартного вида DOM-элемента;" :value="2" />
                <v-radio label="нужно синхронизировать значение полей форм и свойства модели форм для каждого элемента управления формы;" :value="3" />
                <v-radio label="необходимо повторение блока контента в заданной позиции, что может быть полезно для генерирования одного контента в нескольких местах с предотвращением дублирования;" :value="4" />
              </v-radio-group>
            </div>

            <div class="mb-16">
              <h3>
                8. C помощью декоратора @Input() можно:
              </h3>
              <v-radio-group v-model="eighth">
                <v-radio
                  :label="`передать данные из родительского компонента дочернему, сразу на несколько уровней иерархии;`"
                  :value="1"
                />
                <v-radio
                  :label="`передать данные из родительского компонента дочернему, но только на один уровень иерархии;`"
                  :value="2"
                />
                <v-radio
                  :label="`имитировать возникновение события ввода в дочернем компоненте и передать введённые данные родительскому компоненту;`"
                  :value="3"
                />
                <v-radio
                  :label="`передать данные из дочернего компонента родительскому , но только на один уровень иерархии;`"
                  :value="4"
                />
                <v-radio
                  :label="`передать данные из дочернего компонента родительскому , сразу на несколько уровней иерархии;`"
                  :value="5"
                />
                <v-radio
                  :label="`имитировать возникновение события ввода в родительском компоненте и передать введённые данные дочернему компоненту`"
                  :value="5"
                />
              </v-radio-group>
            </div>

            <div class="mb-16">
              <h3>
                9. Укажите основное назначение сервисов в Angular:
              </h3>
              <v-checkbox
                hide-details
                v-model="nineth"
                :label="`хранение данных в памяти;`"
                :value="1"
              />
              <v-checkbox
                hide-details
                v-model="nineth"
                :label="`хранение глобального состояния приложения;`"
                :value="2"
              />
              <v-checkbox
                hide-details
                v-model="nineth"
                :label="`программирование асинхронных потоков данных в декларативном стиле;`"
                :value="3"
              />
              <v-checkbox
                hide-details
                v-model="nineth"
                :label="`инкапсулирование бизнес-логики для решения проблемы повторения кода, если необходимо выполнить одну и ту же задачу в разных компонентах и классах;`"
                :value="4"
              />
              <v-checkbox
                hide-details
                v-model="nineth"
                :label="`получения данных из какого-либо источника данных;`"
                :value="5"
              />
              <v-checkbox
                hide-details
                v-model="nineth"
                :label="`преобразование данных прямо в HTML-шаблоне;`"
                :value="6"
              />
              <v-checkbox
                hide-details
                v-model="nineth"
                :label="`изменение внешнего вида или поведения DOM-элемента;`"
                :value="7"
              />
              <v-checkbox
                hide-details
                v-model="nineth"
                :label="`изолирование логической объединяющей структуры для компонентов, директив и фильтров`"
                :value="8"
              />
            </div>

            <div class="mb-16">
              <h3>10. В чем разница между директивами show и if?</h3>
              <v-radio-group v-model="tenth">
                <v-radio
                  label="if гарантирует, что слушатели событий и дочерние компоненты уничтожаются и воссоздаются при переключениях условия"
                  :value="1"
                />
                <v-radio
                  label="Элемент всегда отрисовывается, вне зависимости от исходного состояния"
                  :value="2"
                />
                <v-radio
                  label="У if выше затраты на переключение, а show имеет больше затрат на первичную отрисовку"
                  :value="3"
                />
                <v-radio label="Все вышеперечисленные" :value="4" />
              </v-radio-group>
            </div>

            <div class="mb-16">
              <h3>11. Выберите модификаторы клавиш мыши</h3>
              <v-checkbox
                hide-details
                v-model="eleventh"
                :label="`up`"
                :value="1"
              />
              <v-checkbox
                hide-details
                v-model="eleventh"
                :label="`middle`"
                :value="2"
              />
              <v-checkbox
                hide-details
                v-model="eleventh"
                :label="`left`"
                :value="3"
              />
              <v-checkbox
                hide-details
                v-model="eleventh"
                :label="`click`"
                :value="4"
              />
              <v-checkbox
                hide-details
                v-model="eleventh"
                :label="`doubleclick`"
                :value="5"
              />
              <v-checkbox
                hide-details
                v-model="eleventh"
                :label="`right`"
                :value="6"
              />
              <v-checkbox
                hide-details
                v-model="eleventh"
                :label="`down`"
                :value="7"
              />
            </div>

            <h3>
              12. Сколько в Angular представлено нативных конструкторов типов?
            </h3>
            <div class="mb-16 mt-10" style="width: 400px">
              <v-slider
                v-model="twelveth"
                max="15"
                min="1"
                step="1"
                hide-details
                thumb-label="always"
              />
            </div>

            <div class="mb-16">
              <h3>
                13. Отметьте неправильный пример использования директивы v-for
              </h3>
              <v-radio-group v-model="thirteen">
                <v-radio
                  :label="`v-for=&quot;(item, index) in items&quot;`"
                  :value="1"
                />
                <v-radio
                  :label="`v-for=&quot;(value, key, index) of user&quot;`"
                  :value="2"
                />
                <v-radio
                  :label="`v-for=&quot;let item in items&quot;`"
                  :value="3"
                />
              </v-radio-group>
            </div>

            <div class="mb-16">
              <h3>
                14. Что верно относительно совместного использования директив
                v-for и v-if?
              </h3>
              <v-checkbox
                hide-details
                v-model="fourteen"
                :label="`Не рекомендуется их совместное использование`"
                :value="1"
              />
              <v-checkbox
                hide-details
                v-model="fourteen"
                :label="`v-if имеет больший приоритет, чем v-for`"
                :value="2"
              />
              <v-checkbox
                hide-details
                v-model="fourteen"
                :label="`v-vor имеет больший приоритет, чем v-if`"
                :value="3"
              />
              <v-checkbox
                hide-details
                v-model="fourteen"
                :label="`В условии v-if не будет доступа к переменным из области видимости v-for`"
                :value="4"
              />
              <v-checkbox
                hide-details
                v-model="fourteen"
                :label="`Всё перечисленное`"
                :value="5"
              />
            </div>

            <div class="mb-16">
              <h3>
                15. Какой из перечисленных методов массивов не запускет
                обновление отображения
              </h3>
              <v-radio-group v-model="fifteen">
                <v-radio label="push()" :value="1" />
                <v-radio label="pop()" :value="2" />
                <v-radio label="shift()" :value="3" />
                <v-radio label="unshift()" :value="4" />
                <v-radio label="splice()" :value="5" />
                <v-radio label="sort()" :value="6" />
                <v-radio label="concat()" :value="7" />
                <v-radio label="reverse()" :value="8" />
              </v-radio-group>
            </div>

            <div class="mb-16">
              <h3>
                16. Укажите правильные утверждения, характерные для паттерна Observer в JavaScript:
              </h3>
              <v-checkbox
                hide-details
                v-model="sixteen"
                label=" паттерн Observer переводится как Издатель-Подписчик;"
                :value="1"
              />
              <v-checkbox
                hide-details
                v-model="sixteen"
                label="паттерн Observer переводится как Наблюдатель;"
                :value="2"
              />
              <v-checkbox
                hide-details
                v-model="sixteen"
                label="идея паттерна Observer заключается в создании зависимости типа один ко многим;"
                :value="3"
              />
              <v-checkbox
                hide-details
                v-model="sixteen"
                label="идея паттерна Observer заключается в создании зависимости типа многие ко многим;"
                :value="4"
              />
              <v-checkbox
                hide-details
                v-model="sixteen"
                label="паттерн Observer применяется тогда, когда необходимо передать запрос на выполнение одному из нескольких объектов, точно не определяя, какому именно объекту;"
                :value="5"
              />
              <v-checkbox
                hide-details
                v-model="sixteen"
                label="для реализации паттерна Observer в Angular используется сторонняя библиотека (RxJS);"
                :value="6"
              />
              <v-checkbox
                hide-details
                v-model="sixteen"
                label="паттерн Observer применяется тогда, когда необходимо добавить новые состояния к классам, при этом не изменяя их общую структуру;"
                :value="7"
              />
              <v-checkbox
                hide-details
                v-model="sixteen"
                label="паттерн Observer характеризуется отсутствием прямой связи между объектами Subject и Observer;"
                :value="8"
              />
              <v-checkbox
                hide-details
                v-model="sixteen"
                label=" паттерн Observer характеризуется наличием прямой связи между объектами Subject и Observer;"
                :value="9"
              />
              <v-checkbox
                hide-details
                v-model="sixteen"
                label=" паттерн Observer характеризуется тем, что существует один наблюдаемый объект и множество наблюдателей. При изменении наблюдаемого объекта автоматически происходит оповещение всех наблюдателей"
                :value="10"
              />
            </div>

            <div class="mb-16">
              <h3>
                17. Какая передача props в качестве входных параметров
                недопустима
              </h3>
              <v-radio-group v-model="seventeen">
                <v-radio :label="`:value=&quot;42&quot;`" :value="1" />
                <v-radio :label="`:value=&quot;false&quot;`" :value="2" />
                <v-radio
                  :label="`:value=&quot;[234, 266, 273]&quot;`"
                  :value="3"
                />
                <v-radio
                  :label="`:author=&quot;{ name: 'Veronica', company: 'Veridian Dynamics' }&quot;`"
                  :value="4"
                />
                <v-radio label="Всё выше перечисленное допустимо" :value="5" />
              </v-radio-group>
            </div>

            <div class="mb-16">
              <h3>
                18. В каких случаях при передаче boolean свойства оно примет
                значение true?
              </h3>
              <v-checkbox
                hide-details
                v-model="eighteen"
                :label="`<TestComponent canShow />`"
                :value="1"
              />
              <v-checkbox
                hide-details
                v-model="eighteen"
                :label="`<TestComponent canShow=&quot;can-show&quot; />`"
                :value="2"
              />
              <v-checkbox
                hide-details
                v-model="eighteen"
                :label="`<TestComponent canShow=&quot;&quot; />`"
                :value="3"
              />
              <v-checkbox
                hide-details
                v-model="eighteen"
                :label="`<TestComponent canShow=&quot;canShow&quot; />`"
                :value="4"
              />
              <v-checkbox
                hide-details
                v-model="eighteen"
                :label="`<TestComponent canShow=&quot;true&quot; />`"
                :value="5"
              />
            </div>

            <div class="mb-16">
              <h3>19. С какой версии Angular основные версии ядра Angular и CLI согласованы?</h3>
              <v-radio-group v-model="nineteen">
                <v-radio
                  :label="`Angular 2`"
                  :value="1"
                />
                <v-radio
                  :label="`Angular 4`"
                  :value="2"
                />
                <v-radio
                  :label="`Angular 5`"
                  :value="3"
                />
                <v-radio
                  :label="`Angular 7`"
                  :value="4"
                />
              </v-radio-group>
            </div>

            <div class="mb-16">
              <h3>20. В чём заключается смысл однофайлового компонента?</h3>
              <v-radio-group v-model="twenty">
                <v-radio
                  :label="`Один такой компонент с его шаблоном, скриптом и стилями находится в одном файле`"
                  :value="1"
                />
                <v-radio
                  :label="`В одном файле содержится код всей страницы. Это очень удобно`"
                  :value="2"
                />
                <v-radio :label="`Оба утверждения верны`" :value="3" />
              </v-radio-group>
            </div>
          </v-form>

          <v-btn
            color="primary"
            @click="handleFormSubmit"
            :disabled="submitDisabled"
            >Отправить</v-btn
          >
        </v-sheet>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import { isEmpty } from "lodash";

export default {
  name: "TestingPage",
  data() {
    return {
      first: [],
      second: 0,
      third: [],
      fourth: [],
      fifth: 0,
      sixth: [],
      seventh: 0,
      eighth: 0,
      nineth: [],
      tenth: 0,
      eleventh: [],
      twelveth: 0,
      thirteen: 0,
      fourteen: [],
      fifteen: 0,
      sixteen: [],
      seventeen: 0,
      eighteen: [],
      nineteen: 0,
      twenty: 0
    };
  },
  computed: {
    submitDisabled() {
      return (
        isEmpty(this.first) ||
        !this.second ||
        isEmpty(this.third) ||
        isEmpty(this.fourth) ||
        !this.fifth ||
        isEmpty(this.sixth) ||
        !this.seventh ||
        !this.eighth ||
        isEmpty(this.nineth) ||
        !this.tenth ||
        isEmpty(this.eleventh) ||
        !this.twelveth ||
        !this.thirteen ||
        isEmpty(this.fourteen) ||
        !this.fifteen ||
        isEmpty(this.sixteen) ||
        !this.seventeen ||
        isEmpty(this.eighteen) ||
        !this.nineteen ||
        !this.twenty
      );
    },
  },
  methods: {
    handleFormSubmit() {
      const answers = [
        this.first,
        this.second,
        this.third,
        this.fourth,
        this.fifth,
        this.sixth,
        this.seventh,
        this.eighth,
        this.nineth,
        this.tenth,
        this.eleventh,
        this.twelveth,
        this.thirteen,
        this.fourteen,
        this.fifteen,
        this.sixteen,
        this.seventeen,
        this.eighteen,
        this.nineteen,
        this.twenty,
      ]

      const sortedAnswers = answers.map((answer, index) => {
        if (index === 8 || typeof answer === 'number') return answer
        return answer.sort()
      })

      this.$store.commit('setAnswers', sortedAnswers)
      this.$router.push({ name: 'testing-testing_results' })
    },
  }
};
</script>
