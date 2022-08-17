<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <h2 class="screen__subtitle">ТРЕНИРОВКИ</h2>
          <div class="screen__content">
            <div class="screen__info">
              <p class="screen__text">Начинать тренировки пакистанских голубей лучше в группе.</p>
              <p class="screen__text">Делается это в несколько этапов:</p>
              <ul class="screen__text">
                <li>молодняк приучают к месту;</li>
                <li>полёты с голубем-вожаком;</li>
                <li>когда голуби освоятся, можно отпускать их на самостоятельные вылеты.</li>
              </ul>
              <p class="screen__text">
                Пакистанцы иногда дезориентируются в пространстве и при отрабатывании кувырков теряют равновесие и высоту, они даже могут разбиться.
              </p>
              <p class="screen__text">
                Если хозяину кажется, что какая-то из птиц плохо держится в небе и есть риск падения, данную особь предлагается «подержать на булавках» - то
                есть стянуть маховые перья.
              </p>
              <p class="screen__text">После обучения голубь не будет терять ориентацию при выполнении элемента.</p>
              <p class="screen__text">Бой у голубей передаётся по наследству.</p>
              <p class="screen__text">
                Бой у птенцов-сверстников может начаться в разном возрасте: от 3 месяцев до 1,5-2 лет. Птиц, которые так и не освоили «высший пилотаж»,
                знатоки называют «простолётами».
              </p>
            </div>
          </div>
          <Navigation :page-next="pageNext" :page-prev="pagePrev"/>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import {mapActions} from 'vuex'
import Navigation from "@/components/Navigation";
import Doves from "@/components/Doves";
import Logo from "@/components/Logo";
import Background from "@/components/Background";

export default {
  name: "Page-5",
  data() {
    return {
      pagePrev: 'page-4',
      pageNext: 'page-6',
    }
  },
  components: {
    Doves,
    Logo,
    Background,
    Navigation
  },
  mounted() {
    this.animate()
  },
  methods: {
    ...mapActions([
      'animate'
    ]),
  }
}
</script>