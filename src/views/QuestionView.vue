<template>
    <div class="relative bsa animate__animated  animate__zoomInDown">
      <div 
        v-for="(item, index) in items" 
        :key="index" 
        class="bg-white rounded-lg p-4"
        @click="toggle(index)"
      >
        <div class="flex items-center justify-between animate__animated  animate__zoomInDown">
          {{ item.title }}
          <div v-if="index === active" class="rotate-180">
            <svg class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
              <path d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414-.707.707L10 13.657l-2.293-2.293z" />
            </svg>
          </div>
          <div v-else>
            <svg class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
            </svg>
          </div>
        </div>
      </div>
      <div 
        v-for="(item, index) in items" 
        :key="index" 
        class="p-4 bg-gray-200"
        v-show="index === active"
      >
        {{ item.content }}
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        active: null,
        items: [
          { title: 'Что мы продаём?', content: 'Наша программа помогает узнать следующий коэфицент в казино игре, тем самым помогаем людям заработать на "серой" схеме заработка. Программа абсолютно безопасна и никакие федералы к вам не прийдут)' },
          { title: 'Когда окупится программа? Сколько я смогу с неё заработать?', content: 'Тут на самом деле все зависит от вашего терпение и баланса на сайте. К примеру возьмем 1000 российских рублей, в день с такой суммой без навязчивых вопрос от модераторов можно заработать до 20.000р.Окупить недельную версию программы вы несомненно можете в первый же день покупки.' },
          { title: 'Можно ли бесплатно протестировать ваш софт?', content: 'К сожалению нельзя. Так как наши программисты добавили функцию временной подписки, софт на час, день я выдать не смогу. Ну выдавать каждому  бесплатный недельный пробник я не собираюсь, иначе какой смысл устраивать все это? Логично ведь, согласитесь.' },
        ],
      }
    },
    methods: {
      toggle(index) {
        if (this.active === index) {
          this.active = null
        } else {
          this.active = index
        }
      },
    },
  }
  </script>
<style>
.bsa{
    margin-top: 10em;
}

</style>
  