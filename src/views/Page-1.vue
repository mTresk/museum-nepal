<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <h2 class="screen__subtitle">Пакистанские голуби</h2>
          <div class="screen__content">
            <div class="screen__images">
              <div style="width: 800px; height: 500px" class="screen__image screen__image-ibg">
                <img src="img/1.jpg" alt="" />
              </div>
            </div>
            <div class="screen__info screen__info_right">
              <p class="screen__text">
                Это одна из самых лучших лётных пород по мнению знатоков-голубеводов. <br />
                Этих птиц часто держат арабы, индусы, заводчики очень гордятся своими голубями, причём не только из-за их внешней красоты. <br />
                Индо-пакистанские голуби известны своей способностью без специфических тренировок выдерживать полёт в воздухе до 12 часов. При этом для
                пакистанского голубя не важна температура воздуха. В условиях жаркого климата они поднимаются ввысь и выдерживают такие нагрузки, когда
                градусник показывает плюс 50°С.
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
import Background from "@/components/Background";
import Logo from "@/components/Logo";
import Doves from "@/components/Doves";

export default {
  name: "Page-1",
  data() {
    return {
      pageNext: 'page-2',
      pagePrev: 'home'
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