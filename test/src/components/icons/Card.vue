<template>
  <div class="Notes">
    <div class="Note-Card">
      <h2>{{ Note }}</h2>
      <h2>{{ Clef }}</h2>
      <img class="Img" :src="Image" alt="Note" />      
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    Note: String,
    Clef: String,
    Image: String,
  },
};
</script>

<style>
.Img {
  width: 37%;
}
.Note-Card {
  width: 30%;
  height: 45%;
  margin: 2rem;
  align-content: center;
}
.Notes {
  display: flex;
  flex-wrap: wrap;
  text-align: center;
  flex-direction: row;
  justify-content: space-evenly;
}
</style>