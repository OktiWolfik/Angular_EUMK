<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card>
      

            <div>
              <h2 class="mt-6">Основы работы с Angular: Ваше первое приложение</h2>
              <v-divider class="mb-6" />
              <p>Добро пожаловать в Angular!</p>
              <p>В этом Обучающем руководстве Вы познакомитесь с основами фреймворка Angular.
                Вы повторите то, что уже знали о HTML и JavaScript—а также о некоторых полезных 
                функциях Angular —которые необходимы для создания Интернет-магазина с каталогом 
                товаров, корзиной для покупок и формой заказа. Устанавливать ничего не нужно: 
                приложение компилируется в онлайн IDE StackBlitz.</p>
              <SuccessAlert>
                НОВИЧОК В ВЕБ-РАЗРАБОТКЕ? 
                Кроме данной информации об Angular, есть еще много других ресурсов. 
                Документация на MDN включает основы работы с HTML и JavaScript. В 
                документации по TypeScript есть 5-минутный тьюториал. На разных онлайн 
                образовательных платформах, например Udemy и Codecademy, также можно 
                найти информацию об основах веб-разработки.
              </SuccessAlert>
            </div>
          </div>

          <div>
            <h2 class="mt-6">Создание нового проекта</h2>
            <v-divider class="mb-6" />
            <p>
              <a href="https://stackblitz.com/angular/vkgjdpjqrdej?file=src%2Fapp%2Fapp.component.ts">Кликните здесь и создайте новый проект в среде программирования 
              StackBlitz.</a>
            </p>
            <div class="d-flex justify-center">
              <v-img
                class="mb-4"
                max-width="260"
                height="248"
                src="https://angular-doc.ru/generated/images/guide/start/new-app.png"
              />
            </div>
            <SuccessAlert>
            <p>СОВЕТЫ ПО ИСПОЛЬЗОВАНИЮ STACKBLITZ</p>
            <p>· Зарегистрируйтесь в StackBlitz, чтобы иметь возможность сохранять 
            и возобновлять свою работу. На StackBlitz можно зайти через учетную запись GitHub, если она есть.</p>
            <p>· Чтобы скопировать пример кода из этого Обучающего руководства, нажмите на иконку в верхнем правом 
            углу элемента примера кода, а затем вставьте фрагмент исходного кода из буфера хранения в StackBlitz.</p>
            <p>· Если в области предварительного просмотра в StackBlitz отображается не то, что вы ожидали, сохраните, 
            а затем нажмите на кнопку обновления страницы.</p>
            <p>· StackBlitz постоянно улучшается, поэтому могут быть незначительные изменения в генерируемом коде, 
            но принцип работы приложения остается неизменным.</p></SuccessAlert>
          </div>

          <div>
            <h2 class="mt-6">Синтаксис шаблонов</h2>
            <v-divider class="mb-6" />
            <p>
              Синтаксис шаблона Angular расширяет HTML и JavaScript. В этом разделе 
              Вы узнаете о синтаксисе шаблонов через расширение функционала области "Товары".
            </p>
            <p>(Чтобы Вы могли полностью погрузиться в синтаксис шаблонов, в дальнейшем используются 
                подготовленные данные о товарах и методы из файла product-list.component.ts.)</p>
            <p>1. В папке product-list откройте файл шаблонов product-list.component.html.</p>
            <p>2. Измените шаблон списка товаров для представления списка названий товаров.</p>
                </p>2.1 Товары в списке должны отображаться одинаково, друг за другом на странице. 
                Для этого воспользуйтесь директивой *ngFor. Установите директиву *ngFor на <code>&lt;div></code>, как представлено ниже:</p>
            
            <p>src/app/product-list/product-list.component.html</p>
            <p><div class="language-html line-numbers-mode">
              <pre
                class="language-html"
              ><span class="tag">&lt;h2&gt;</span><span class="pln">Products</span><span class="tag">&lt;/h2&gt;</span>
              
<span class="pln"><span class="tag">&lt;div</span><span class="pln"> *</span><span class="atn">ngFor</span><span class="pun">=</span><span class="atv">"let product of products"</span><span class="tag">&gt;</span><span class="pln">
<span class="tag">&lt;/div&gt;</span></p>
</span>  
</span>
</code></pre>
            </div>
           
            <p>
              Благодаря директиве *ngFor для каждого товара в списке повторяется <code>&lt;div></code>.
            </p>
            <SuccessAlert>
                *ngFor это "структурная директива". Структурные директивы определяют 
                или меняют структуру DOM за счет добавления, удаления или изменения 
                элементов, к которым они прикрепляются. Любая директива
                с * - структурная директива.
              </SuccessAlert>
            <p>2.2 Для отображения названий товаров используйте синтаксис интерполяции {{ }}. 
                Интерполяция определяет значение свойства как текст. Внутри <code>&lt;div></code> 
                добавьте заголовок <code>&lt;h3></code> для отображения наименования товара:</p>
             <div class="d-flex justify-left">
            <v-img max-width="367" :src="image1" />
          </div>
          <p>Область предварительного просмотра обновляется, и в списке отображается название каждого товара.</p>
          <div class="d-flex justify-center">
              <v-img
                class="mb-4"
                max-width="259"
                height="271"
                src="https://angular-doc.ru/generated/images/guide/start/template-syntax-product-names.png"
              />
            </div>
            <p>2.3 В окончательной версии приложения название товара представляет собой активную ссылку, 
                которая ведет к подробной информации о товаре. Сейчас добавьте ссылку, при этом задайте 
                название ссылки аналогичным названию товара за счет использования синтаксиса привязки свойства [ ], 
                как показано ниже:</p>
           <div class="d-flex justify-left">
            <v-img max-width="399" :src="image2" />
           </div>
           <p>2.4 Добавьте описание товаров. В теге параграфа используйте директиву *ngIf для того, 
            чтобы элемент параграфа создавался только при наличии описания у текущего товара.</p>
            <div class="d-flex justify-left">
            <v-img max-width="407" :src="image3" />
           </div>
           <p>Сейчас в приложении отображается название и описание каждого товара в списке, 
            как показано ниже. Обратите внимание, что в окончательной версии у товара совсем 
            отсутствует параграф с описанием. Поскольку свойство описания товара пустое, 
            элемент параграфа—включая слово "Описание"—не создается.</p>
            <div class="d-flex justify-center">
              <v-img
                class="mb-4"
                max-width="259"
                height="289"
                src="https://angular-doc.ru/generated/images/guide/start/template-syntax-product-description.png"
              />
            </div>
            <p>2.5 Добавьте кнопку, чтобы пользователи могли поделиться товаром с друзьями. 
              Свяжите событие кнопки click с событием share(), которые мы определили за Вас 
              (в product-list.component.ts). Привязка событий происходит за счет заключения события 
              в скобки ( ), как показано ниже:</p>
            <div class="d-flex justify-left">
            <v-img max-width="467" :src="image4" />
           </div>  
           <p>У каждого товара сейчас есть кнопка "Поделиться":</p>
           <div class="d-flex justify-center">
              <v-img
                class="mb-4"
                max-width="259"
                height="376"
                src="https://angular-doc.ru/generated/images/guide/start/template-syntax-product-share-button.png"
              />
            </div>
            <p>Попробуйте кликнуть на кнопку "Поделиться":</p>
            <div class="d-flex justify-center">
              <v-img
                class="mb-4"
                max-width="330"
                height="104"
                src="https://angular-doc.ru/generated/images/guide/start/template-syntax-product-share-alert.png"
              />
            </div>
            <p>В приложении сейчас есть список товаров, и функция поделиться товаром. 
              Вы научились использовать пять стандартных наборов функций синтаксиса шаблона Angular:</p>
            <p>· *ngFor</p>
            <p>· *ngIf</p>
            <p>· Интерполяция {{ }}</p>
            <p>· Привязка свойства [ ]</p>
            <p>· Привязка события ( )</p>
          </div>

          <div>
            <h2 class="mt-6">Компоненты</h2>
            <v-divider class="mb-6" />
            <p>Компоненты определяют области ответственности в пользовательском интерфейсе, 
              что позволит Вам многократно использовать эти наборы функциональных возможностей 
              интерфейса. Вы уже создали один компонент со списком товаров.</p>
            
            <p>
              Компонент состоит их трех элементов:
            </p>
            <p>
             · Класс компонента управляет данными и функциональностью. В предыдущем разделе в классе компонента для Вас были определены данные товаров и метод share().</p>
             <p>· HTML-шаблон определяет, что видит пользователь. В предыдущем разделе Вы изменили HTML-шаблон списка товаров для отображения названия, описания и кнопки "Поделиться" для каждого товара.</p>
             <p>· Компонентно-ориентированные стили определяют внешний вид. Список товаров не определял стили.
            </p>
            <p>Приложение на Angular представляет собой дерево компонентов, в котором у каждого компонента Angular есть особая цель и область ответственности.</p>
            <p>Сейчас у нашего приложения есть три компонента:</p>
            <div class="d-flex justify-center">
              <v-img
                class="mb-4"
                max-width="324"
                height="527"
                src="https://angular-doc.ru/generated/images/guide/start/app-components.png"
              />
            </div>
            <p>· app-root (оранжевый блочный элемент) – оболочка приложения. Это первый компонент для загрузки и родитель для всех других компонентов. Можно считать компонент базовой страницей.</p>
            <p>· app-top-bar (голубой фон) – название магазина и кнопка выхода из приложения.</p>
            <p>· app-product-list (фиолетовый блочный элемент) – список товаров, которые Вы изменили в предыдущем разделе.</p>
            </div>

          <div>
            <h2 class="mt-6">Исходная информация</h2>
            <v-divider class="mb-6" />
            <p>
              В настоящий момент в списке товаров отображается название и описание по каждому товару. 
              Вероятно, Вы заметили, что компонент списка товаров также определяет свойство products, 
              которое содержит импортированные данные для каждого товара (См. группу products в products.ts.)
           </p>
           <p>Мы создадим новую опцию оповещения, при этом товар будет восприниматься как исходная информация. 
            Цены товара отслеживаются, и при цене товара выше $700 отображается кнопка "Оповестить", 
            при нажатии на которую пользователь подписывается на оповещения о снижении цены на товар.
 </p>
          <p>1. Создайте новый компонент товара об оповещениях.</p>
          <p>1.1 Кликните правой кнопкой мышки на папку app и используйте 
            Angular Generator для генерации нового компонента под названием product-alerts.</p>

            <div class="d-flex justify-center">
              <v-img
                class="mb-4"
                max-width="259"
                height="368"
                src="https://angular-doc.ru/generated/images/guide/start/generate-component.png"
              />
            </div>
            <p>Генератор создаст базовые файлы для всех трех частей компонента:
              <br>
              <br>
              · product-alerts.component.ts<br>
              · product-alerts.component.html<br>
              · product-alerts.component.css</p>
            <p>
              2. Откройте product-alerts.component.ts.
            </p>
            <div class="d-flex justify-left">
            <v-img max-width="510" :src="image5" />
           </div>
           <p>2.1 Обратите внимание на декоратор @Component, который указывает на то, что следующий класс является компонентом. Он обеспечивает метаданные о компоненте, включая его шаблоны, стили и селектор.

           <br><br>· selector используется для определения компонента. Селектор – имя, данное Вами компоненту Angular, когда он отображается на странице как HTML-элемент. Как правило, селектор компонента Angular начинается с префикса app-, затем идет название компонента.

           <br>· Шаблон и имя файлов со стилями – это еще два других файла, которые были сгенерированы для Вас.<br>
           2.2 Определение компонента также включает экспортированный класс (ProductAlertsComponent), который управляет функциональностью компонента.</p>
          </div>

          <v-btn
            class="mt-6"
            color="success"
            nuxt
            to="/guide/3 route"
          >
            Следующий раздел
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

<script>
import image1 from '~/assets/screens/im1.png';
import image2 from '~/assets/screens/im2.png';
import image3 from '~/assets/screens/im3.png';
import image4 from '~/assets/screens/im4.png';
import image5 from '~/assets/screens/im5.png';


export default {
  name: "CodeScreen",
  data() {
    return {
      image1,
      image2,
      image3,
      image4,
      image5

    }
  }
};
</script>