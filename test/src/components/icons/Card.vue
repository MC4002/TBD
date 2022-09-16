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
h2 {
  font-size: 1rem;
  text-align: center;
}
.Img {
  width: 100%;
}
.Note-Card {
  width: 30%;
  height: 45%;
  margin-top: 20px;
  margin-bottom: 20px;
}
.Notes {
  display: flex;
  flex-wrap: wrap;
  text-align: center;
  flex-direction: row;
  align-content: center;
  justify-content: space-evenly;
}
</style>