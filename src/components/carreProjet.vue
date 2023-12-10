<template>
  <div id="projet">
    <div id="texte">
      <h1>{{ titre }}</h1>
      <h2>{{ sousTitreFR }}</h2>
    </div>
    <div id="img">
      <img
        src="https://freight.cargo.site/w/1500/q/75/i/aeda44fab5b3661781ee65a8ade38b028435163c56b9a07688c3e07e4793beca/DSCF3384.jpg"
        alt=""
      />
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
  },
};
</script>

<style>
#projet {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  height: 70vh;
}

#texte {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
  background-color: #fdf5ee;
}

#img {
  display: flex;
  justify-content: center;
  align-items: center;
  height: inherit;
  width: 100%;
  background-color: #b1b5fa;
  grid-column-start: 1;
  grid-row-start: 1;
}

#img img {
  max-width: 70%;
  max-height: 70%;
}
</style>
