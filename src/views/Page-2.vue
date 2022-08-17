<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <h2 class="screen__subtitle">Внешний вид</h2>
          <div class="screen__content">
            <div class="screen__images">
              <div style="width: 800px; height: 500px" class="screen__image screen__image-ibg">
                <img src="img/2.jpg" alt="" />
              </div>
            </div>
            <div class="screen__info screen__info_right">
              <p class="screen__text">У пакистанского бойного голубя очень аккуратная внешность.</p>
              <p class="screen__text">
                Индопакистанские представители всегда имеют длинный хвост, которым не могут похвастать другие высоколётные голуби. Состоит он не менее, чем
                из 12 перьев. Пакистанские бойные голуби внешне чрезвычайно отличаются друг от друга, что делает их еще более неповторимыми и популярными.
              </p>
              <p class="screen__text">К общим характеристикам вида относятся:</p>
              <ul class="screen__text">
                <li>крепкое тело с широкой грудной клеткой;</li>
                <li>миниатюрная голова;</li>
                <li>средний размер;</li>
                <li>перо белого цвета с рисунком, который сохраняется на нём на всю жизнь;</li>
                <li>удлинённый хвост;</li>
                <li>крыло с чёрным окрасом по краю.</li>
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
import Background from "@/components/Background";
import Logo from "@/components/Logo";
import Doves from "@/components/Doves";

export default {
  name: "Page-2",
  data() {
    return {
      pagePrev: 'page-1',
      pageNext: 'page-3',
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