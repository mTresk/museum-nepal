<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <h2 class="screen__subtitle">Полет</h2>
          <div class="screen__content">
            <div class="screen__images">
              <div style="width: 800px; height: 500px" class="screen__image screen__image-ibg">
                <img src="img/4.jpg" alt="" />
              </div>
            </div>
            <div class="screen__info screen__info_right">
              <p class="screen__text">
                Первое, что стоит отметить, это необычный стиль полёта пакистанских голубей. Именно благодаря ему птицы получили всемирную известность и
                популярность. Такой стиль встречается только у этого вида.
              </p>
              <h2 class="screen__subtitle screen__subtitle_h3">Наиболее узнаваемые акробатические фигуры</h2>
              <ul class="screen__text">
                <li>
                  Долгое зависание в воздухе. При этом птицы поднимаются так высоко, что разглядеть их с земли бывает проблематично. «Пакистанцы» замирают
                  на месте с распростёртыми крыльями.
                </li>
                <li>Кувырки, сопровождаемые боем – громким хлопаньем крыльев.</li>
                <li>Прыжки в воздухе. С каждым новым сальто голубь может подниматься всё выше, что называется «выходить в столб».</li>
              </ul>
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
  name: "Page-4",
  data() {
    return {
      pagePrev: 'page-3',
      pageNext: 'page-5',
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