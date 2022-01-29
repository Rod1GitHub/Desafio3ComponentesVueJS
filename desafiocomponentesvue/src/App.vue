<template>
  <div id="app-desafio-componentes">
    <ul>
      <li
        v-for="(characterArgument005, index005) in charactersPluralArray005"
        :key="index005"
      >
        <img :src="getUrlImageMethod005(characterArgument005)" />
        <p>{{ characterArgument005.name }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      charactersPluralArray005: [
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
    getUrlImageMethod005(characterParam005) {
      return `https://rickandmortyapi.com/api/character/avatar/${characterParam005.id}.jpeg`;
    },
  },
};
</script>

<style>
#app-desafio-componentes {
  font-family: Arial;
}
body {
  background: no-repeat center fixed
    url("https://rickandmortypod.com/wp-content/uploads/2018/11/cropped-RM_page-header_background1-3.png");
}
ul {
  color: green;
  font-size: 20px;
}

img {
  border: 1px solid green;
  height: 50px;
  width: 50px;
  border-radius: 50%;
}
</style>
