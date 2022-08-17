<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <div class="screen__content">
            <div class="screen__images">
              <div style="width: 800px; height: 500px" class="screen__image screen__image-ibg">
                <img src="img/3.jpg" alt="" />
              </div>
            </div>
            <div class="screen__info screen__info_right">
              <p class="screen__text">Отличительная черта пакистанских голубей - разница в цвете туловища и частей тела (головы, крыльев, шеи).</p>
              <p class="screen__text">Присутствие чуба — условие внутривидового различия, как и оперение на лапах.</p>
              <p class="screen__text">
                Цветовые характеристики сохраняются птицей с момента рождения, не претерпевая изменений. Перья окрашиваются в оттенки красной, металлической
                светлой, голубой, чёрной и оранжевой гаммы.
              </p>
              <p class="screen__text">Цвет глаз может быть голубым, чёрным, оранжевым, красным.</p>
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
  name: "Page-3",
  data() {
    return {
      pagePrev: 'page-2',
      pageNext: 'page-4',
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