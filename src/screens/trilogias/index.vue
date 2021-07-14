<template>
  <nb-container :style="{ backgroundColor: '#fff' }">
    <nb-header>
      <nb-left>
        <nb-button
          transparent
          :onPress="() => this.props.navigation.openDrawer()"
        >
          <nb-icon name="menu" />
        </nb-button>
      </nb-left>
      <nb-body>
        <nb-title>Trilogias</nb-title>
      </nb-body>
      <nb-right /> 
    </nb-header>

    <nb-content padder>
      <nb-text class="titulo">I. A História de Darth Vader</nb-text>
      <nb-text class="subtitulo">Episódios I, II e III</nb-text>
      <!-- <image :source="require('dart-vader.jpeg')" /> -->
      <nb-text
        >Apesar de ter sido lançada depois da trilogia original, essa é a
        primeira trilogia na ordem cronológica da série Star Wars. Nela é
        contada a história do grande vilão Darth Vader.</nb-text
      >
      <nb-text>Saiba de onde ele veio e quem ele é</nb-text>

      <nb-text class="titulo">II. A História de Luke Skywalker</nb-text>
      <nb-text class="subtitulo">Episódios IV, V e VI</nb-text>
      <!-- <image :source="require('dart-vader.jpeg')" /> -->
      <nb-text>Essa foi primeira trilogia da saga, porém sua história se passa após a trilogia I.</nb-text>
      <nb-text>Nela Luke Skywalker se aventura pela galáxia para atender a um pedido de socorro da princesa Leia e batalha contra Darth Vader.</nb-text>

      <nb-text class="titulo">III. A História de Rey</nb-text>
      <nb-text class="subtitulo">Episódios VII, VIII e IX</nb-text>
      <!-- <image :source="require('dart-vader.jpeg')" /> -->
      <nb-text>Enquanto surge uma nova ameaça para a galáxia, Rey, uma catadora de sucata, e Finn, um soldado imperial desertor, devem se juntar a Han Solo e Chewbacca para procurar a única esperança de restaurar a paz da galáxia.</nb-text>
    </nb-content>

    <nb-footer>
      <nb-footer-tab>
        <nb-button active full>
          <nb-text>Trilogias Star Wars</nb-text>
        </nb-button>
      </nb-footer-tab>
    </nb-footer>
  </nb-container>
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
</style>
