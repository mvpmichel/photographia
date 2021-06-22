<template>
  <v-content>
    <div class="staticHero">
      <v-img src="../assets/images/img13.jpg">
        <v-row align="end" class="lightbox white--text pa-2 fill-height">
          <v-col>
            <v-container>
              <div class="headline">Sobre</div>
            </v-container>
          </v-col>
        </v-row>
      </v-img>
    </div>
    <div class="block">
      <v-container>
        <p>Deserunt non reprehenderit non in sint laborum enim Lorem magna qui labore tempor anim culpa. Laborum laboris excepteur labore eu in laborum anim minim. Velit in pariatur reprehenderit minim est sit aliquip exercitation ipsum quis culpa tempor commodo veniam. Esse et nostrud magna pariatur ea esse commodo enim et enim pariatur. Do ex minim consequat minim eu Lorem adipisicing sunt.</p>
      </v-container>
    </div>
    <div class="block">
      <v-container>
        <h2 class="text-center">Nosso time</h2>
        <v-row>
          <v-col v-for="item in items" :key="item.id" class="d-flex child-flex" cols="12" sm="4">
            <v-card flat tile class="mx-auto">
              <v-img :src="item.src" aspect-ratio="1" class="grey lighten-2"></v-img>
              <v-card-text class="text--primary text-center">
                <div class="title">{{ item.name }}</div>
                <p>{{ item.title }}</p>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </v-content>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      items: [
        {
          id: 1,
          src: require("../assets/images/team1.jpg"),
          name: 'Peter Smith',
          title: 'Diretor'
        },
        {
          id: 2,
          src: require("../assets/images/team2.jpg"),
          name: 'Roy Perry',
          title: 'Fotógrafo'
        },
        {
          id: 3,
          src: require("../assets/images/team3.jpg"),
          name: 'Lisa White',
          title: 'Freelancer'
        }
      ]
    };
  }
};
</script>