<template>
  <div id="app-desafio-componentes">
    <ul>
      <li v-for="(character, i) in characters" :key="i">
        <img :src="getImageMethod(character)"/>
        <p>{{ character.name }}</p>
      </li>
    </ul>
  </div>
</template>


<script>
export default {
  name: "App",
  data() {
    return {
      characters: [
        {
          id: 160,
          name: "Hunter's Father",
        },
        {
          id: 302,
          name: "Ruben",
        },
        {
          id: 326,
          name: "Slippery Stair",
        },
        {
          id: 508,
          name: "Fascist Teddy Bear Rick’s Clone",
        },
        {
          id: 520,
          name: "Wasp Jerry",
        },
        {
          id: 676,
          name: "Japheth's Middle Son",
        },
        
      ],
    };
  },
  methods: {
    getImageMethod(character) {
      return `https://rickandmortyapi.com/api/character/avatar/${character.id}.jpeg`;
    },
  },
};
</script>

<style>
#app-desafio-componentes {
  font-family:Arial;
}
body {
  background: no-repeat center fixed url("https://rickandmortypod.com/wp-content/uploads/2018/11/cropped-RM_page-header_background1-3.png");
}
ul {
  color: green;
  font-size:20px;
}


img {
  border: 1px solid green;
  height: 50px;
  width: 50px;
  border-radius: 50%;
}
</style>
