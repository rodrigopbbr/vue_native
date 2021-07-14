<template>

 <nb-container :style="{ backgroundColor: '#fff' }">
    <nb-header>
      <nb-left>
        <nb-button transparent :onPress="() => this.props.navigation.goBack()">
          <nb-icon name="arrow-back" />
        </nb-button>
      </nb-left>
      <nb-body>
        <nb-title>Sobre</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>

    <nb-content padder>
      <nb-card class="mb-15">
        <nb-card-item>
          <nb-body>
            <nb-text class="subtitulo">Aplicativo demostrando algumas funcionalidades do Vue
          Native</nb-text>
          </nb-body>
        </nb-card-item>
      </nb-card>
      
      <nb-card class="mb-15">
        <nb-card-item>
          <nb-body>
            <nb-text class="subtitulo">Tecnologias utilizadas</nb-text>
            <nb-text>Vue Native v. 0.2</nb-text>
            <nb-text>Native Base v. 2</nb-text>
            <nb-text>Vue Native Router  v. 0.2</nb-text>
            <nb-text>React v. 16</nb-text>
          </nb-body>
        </nb-card-item>
      </nb-card>      

      <nb-card class="mb-15">
        <nb-card-item>
          <nb-body>
            <nb-text>Pós-Graduação Lato Sensu</nb-text>
            <nb-text>Convênio TRE/BA - UFBA</nb-text>
          </nb-body>
        </nb-card-item>
      </nb-card>      

      <nb-card class="mb-15">
        <nb-card-item>
          <nb-body>
            <nb-text>Equipe</nb-text>
            <nb-text>Pedro Augusto Vitor de Santana</nb-text>
            <nb-text>Rilson Barros de Almeida</nb-text>
            <nb-text>Rodrigo Pereira Souza</nb-text>
          </nb-body>
        </nb-card-item>
      </nb-card>      

      <nb-card class="mb-15">
        <nb-card-item>
          <nb-body>
            <nb-text>Salvador, Julho de 2021</nb-text>
          </nb-body>
        </nb-card-item>
      </nb-card>      
    </nb-content>

    <nb-footer>
      <nb-footer-tab>
        <nb-button active full>
          <nb-text>Trilogias Star Wars</nb-text>
        </nb-button>
      </nb-footer-tab>
    </nb-footer>

</template>

<style scoped>
.titulo {
  color: yellow;
  background-color: black;
  font-size: 20px;
  margin-top: 15px;
  margin-bottom: 10px;
  text-align: center;
}
.subtitulo {
  font-size: 18px;
  font-weight:bold;
}
.mb-15 {
  margin-bottom: 15;
}
.card-item-image {
  align-self: center;
  height: 150;
}
</style>