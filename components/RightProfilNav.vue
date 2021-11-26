<template>
  <div>
    <v-navigation-drawer class="pa-4 mt-6" app clipped floating permanent right v-model="drawer">
      <v-layout>
        <v-card
          height="300"
          width="100%"
        >
          <v-img
            height="300"
            width="100%"
            src="https://media-exp1.licdn.com/dms/image/C4D03AQFBizn8RyO64A/profile-displayphoto-shrink_100_100/0/1618924385153?e=1643241600&v=beta&t=M1uxCBDOo0AnFObYDaZRF_h32xlPzR5yd3fzheMnzbU"
          />
        </v-card>
      </v-layout>
      <v-row class="mt-6">
        <v-col>
          <div class="title text-uppercase">Arthur Leloup</div>
        </v-col>
      </v-row>
      <v-row>
        <v-col class="subtitle-2">
          3 <span class="grey--text">Photos</span>
        </v-col>
        <v-col class="subtitle-2">
          350 <span class="grey--text">Followers</span>
        </v-col>
      </v-row>
      <v-row>
        <v-col v-if="!granted" class="subtitle-2 grey--text">
          Hi, I'm Arthur. A Junior web Developer.
        </v-col>
      </v-row>
      <v-row>
        <v-col class="subtitle-2">
          Locations <br>
          <span class="subtitle-2 grey--text">
          Based in Amsterdam.
        </span>
        </v-col>
      </v-row>
      <v-row>
        <v-col class="subtitle-2">
          Profession <br>
          <span class="subtitle-2 grey--text">
          Web Developer
        </span>
        </v-col>
      </v-row>
      <v-row>
      </v-row>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      password: null,
    }
  },
}
</script>
