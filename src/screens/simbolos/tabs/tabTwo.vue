<template>
  <nb-content padder>
    <nb-card>
      <nb-card-item>
        <image
          :source="cardImage"
          class="card-item-image"
          :style="stylesObj.cardItemImage"
        />
        <nb-body>
          <nb-text
            >A República Galáctica era aliada da Ordem Jedi e governava o
            universo através do Senado Galático de forma pacífica e justa. O seu
            símbolo significa a excelência do papel desempenhado pela República
            e a sua persistência.</nb-text
          >
        </nb-body>
      </nb-card-item>
      <nb-card-item>
        <nb-body>
          <nb-text
            >A insígnia da República tem origem na Ordem dos Bedu, uma
            organização que se dedicava a entender a Força antes da existência
            da República Galáctica. O símbolo é uma representação do número
            nove, com seus oito raios ligados a um disco único. O grupo
            acreditava que o número significava a presença da Força numa galáxia
            unida.</nb-text
          >
        </nb-body>
      </nb-card-item>
    </nb-card>
    <nb-footer>
      <nb-footer-tab>
        <nb-button active full>
          <nb-text>Trilogias Star Wars</nb-text>
        </nb-button>
      </nb-footer-tab>
    </nb-footer>
  </nb-content>
</template>

<script>
import { Dimensions } from "react-native";
// import logo from "../../../assets/logo.png";
import cardImage from "../../../../assets/simbolos/simb_rep_galactica.png";

const deviceWidth = Dimensions.get("window").width;
export default {
  data() {
    return {
      // logo,
      cardImage,
      stylesObj: {
        cardItemImage: {
          resizeMode: "cover",
          flex: 1,
          width: deviceWidth / 1.18,
        },
      },
    };
  },
};
</script>

<style>
.card-item-image {
  align-self: center;
  height: 150;
}
</style>
