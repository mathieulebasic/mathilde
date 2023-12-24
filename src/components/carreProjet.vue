<template>
  <div id="projet" :class="[theme, dispositionTexte]">
    <div id="texte" :style="{ 'background-color': couleurscoteTexte }">
      <h2>{{ sousTitreEN }}</h2>
      <h1>{{ titre }}</h1>
      <h2>{{ sousTitreFR }}</h2>
    </div>
    <div id="img" :style="{ 'background-color': couleurscoteImage }">
      <img :src="require(`@/assets/hp/` + imageURL)" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "carreProjet",
  props: {
    titre: {
      type: String,
      default: "titre",
    },
    sousTitreFR: {
      type: String,
      default: "sous titre FR",
    },
    sousTitreEN: {
      type: String,
      default: "sous titre EN",
    },
    imageURL: {
      type: String,
      default: "folie.jpg",
    },
    theme: {
      type: String,
      default: "theme1",
    },
    dispositionTexte: {
      type: String,
      default: "droite",
    },
    couleurscoteImage: {
      type: String,
      default: "#fdf5ee",
    },
    couleurscoteTexte: {
      type: String,
      default: "#b1b5fa",
    },
  },
};
</script>

<style>
#projet {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  height: 70vh;
}

.theme1 #texte {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 16px;
  height: 100%;
  width: 100%;
}

.gauche #texte {
  grid-column-start: 1;
  grid-row-start: 1;
}

.droite #texte {
  grid-column-start: 2;
  grid-row-start: 1;
}
.theme1 #img {
  display: flex;
  justify-content: center;
  align-items: center;
  height: inherit;
  width: 100%;
}

#img img {
  max-width: 70%;
  max-height: 70%;
}
</style>
