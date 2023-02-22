<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-card>
        <v-sheet class="pa-4">
          <h1>Практические задания</h1>
          <hr class="my-3" />

          <h3 class="mb-4">1. Работа с переменными</h3>
          <p>
            Дан объект с юзером:
          </p>
          <div class="d-flex justify-center">
            <v-img max-width="233" :src="image1" />
          </div>
          <p>
            Выведите данные из этого объекта как показано ниже:
          </p>
          <div class="d-flex justify-center">
            <v-img max-width="227" :src="image2" />
          </div>

          <h3 class="mb-4 mt-12">2. Работа с массивами</h3>
          <p>
            Дан массив городов и их стран:
          </p>
          <div class="d-flex justify-center">
            <v-img max-width="225" :src="image3" />
          </div>
          <p>
            Выведите эти города в виде списка <code>&lt;ul></code> как показано ниже:
          </p>
          <div class="d-flex justify-center">
            <v-img max-width="253" :src="image4" />
          </div>

          <h3 class="mb-4 mt-12">3. Работа с событиями</h3>
          <p>
            Дана переменная $scope.name со значением 'Иван'. По заходу на страницу 
            запишите эту переменную в абзац. Сделайте ссылку, по клику на которую 
            'Иван' поменяется на 'Дима'.
          </p>
        </v-sheet>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import image1 from '~/assets/images/ex1.png';
import image2 from '~/assets/images/ex11.png';
import image3 from '~/assets/images/ex2.png';
import image4 from '~/assets/images/ex3.png';

export default {
  name: "PracticePage",
  data() {
    return {
      image1,
      image2,
      image3,
      image4
    }
  }
};
</script>
