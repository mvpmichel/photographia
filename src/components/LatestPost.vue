<template>
  <div class="block latestPostBlock">
    <v-container>
      <h2 class="text-center">Ultimas Postagens</h2>
      <v-row>
        <v-col v-for="item in items" :key="item.id" cols="12" md="4">
          <v-card outlined class="mx-auto">
            <v-img
              class="white--text align-end"
              height="200px"
              :src="item.src"
            >
              <v-card-title>{{ item.title }}</v-card-title>
            </v-img>
            <v-card-subtitle class="pb-0">{{ item.subtitle }}</v-card-subtitle>
            <v-card-text class="text--primary">
              <div>{{ item.description }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn color="primary" text>Mais</v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "LatestPost",
  data: () => ({
    show: false,
    items: [
      {
        id: 1,
        title: "Lorem Ipsum",
        subtitle: "aliqua laboris",
        description: "velit magna commodo qui in. Veniam occaecat minim incididunt laborum esse esse aute. Id sint in aliquip ex dolor dolore minim quis consectetur aliqua occaecat velit.",
        src: require("../assets/images/img10.jpg")
      },
      {
        id:21,
        title: "Lorem Ipsum",
        subtitle: "aliqua laboris",
        description: "velit magna commodo qui in. Veniam occaecat minim incididunt laborum esse esse aute. Id sint in aliquip ex dolor dolore minim quis consectetur aliqua occaecat velit.",
        src: require("../assets/images/img11.jpg")
      },
      {
        id: 3,
        title: "Lorem Ipsum",
        subtitle: "aliqua laboris",
        description: "velit magna commodo qui in. Veniam occaecat minim incididunt laborum esse esse aute. Id sint in aliquip ex dolor dolore minim quis consectetur aliqua occaecat velit.",
        src: require("../assets/images/img12.jpg")
      }
    ]
  })
};
</script>