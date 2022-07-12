<template>
  <b-card-group deck>

    <b-card v-for="item in catalog" :key="item"
      :title="item.name"
      :img-src="item.img_src"
      img-alt="Dept"
      img-top
      style="max-width: 20rem"
      footer-tag="footer"
    >
      <b-card-text>
        {{item.describe}}
      </b-card-text>

      <footer style="padding:1rem;">
          <b-button href="#" variant="primary" class="cardBtn"
        >前往＞</b-button
      >
        </footer>

      
    </b-card>
  </b-card-group>

</template>

<script>
//import { defineComponent } from '@vue/composition-api'
import eeImg from "../assets/catalog/電機學群.jpg"
import itImg from "../assets/catalog/資訊學群.jpg"
import lawImg from "../assets/catalog/法政學群.jpg"


export default {
  name: "DeptCard",
  components: {},
  data() {
    return {
      catalog: [
        {
          num: "1",
          name:"電機學群",
          img_src:eeImg,
          describe:"電機是機械能與電能之間轉換裝置的通稱。轉換是雙向的，大部分應用的是電磁感應原理。"
        },
        {
          num: "2",
          name:"資訊學群",
          img_src:itImg,
          describe:"為一切與電腦相關的軟硬體行業總稱，有硬體製造的類似傳統工業模式也有軟體撰寫和客戶服務的服務業"
        },
        {
          num: "3",
          name:"法政學群",
          img_src:lawImg,
          describe:"是一種由規則組成的體系，經由社會組織來施予強制力量，規範個人行為"
        },
        {
          num: "4",
          name:"電機學群",
          img_src:eeImg,
          describe:"電機是機械能與電能之間轉換裝置的通稱。轉換是雙向的，大部分應用的是電磁感應原理。"
        },
      ],
    };
  },
};
</script>


<style scoped>
.cardBtn{
    position: absolute;
    bottom: 0px;
    right: 0px;
    float: right;
}
</style>