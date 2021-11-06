<template>
  <q-page class="flex flex-center justify-center">
    <q-card class="q-ma-lg" flat>
      <q-card-section>
        <div class="text-h6">Мы проводим опросы, которые помогают нам:</div>
        <ul>
          <li>отслеживать тренды в жизни event-индустрии</li>
          <li>разобраться в потребностях нашей целевой аудитории</li>
          <li>собирать материал, чтобы делиться полезной и интересной статистикой</li>
        </ul>
        <p>Если у вас есть опыт в посещении, организации или выступлениях на мероприятиях,
           посмотрите несколько активных опросов ниже и примите участие в небольшом исследовании.</p>
      </q-card-section>

      <q-card-section>
        <q-card class="forms-card" >
          <q-img src="https://atawaka.storage.yandexcloud.net/resize_cache/27313/655929bf7eb695a64fb25e1ae6795806/events-temp/a3b/a3b504cf8fd5c5fb507ce54ae2c2b1fb.jpg"/>

          <q-card-section>
            <div class="text-h6">Инструменты организатора</div>
            <div class="text-subtitle text-grey" >Автор: Семён Быстров</div>
            <p>Форма, в которой мы изучаем инструменты, используемые организатором при разработке мероприятия</p>
          </q-card-section>
          <q-card-actions>
            <q-space/>
            <q-btn label="Пройти" color="primary" icon="quiz" size="md" to="/organizers"/>
          </q-card-actions>
        </q-card>
      </q-card-section>
    </q-card>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'PageIndex'
})
</script>

<style scoped lang="css">

.forms-card {
  width: 100%;
  max-width: 300px;
}
</style>
