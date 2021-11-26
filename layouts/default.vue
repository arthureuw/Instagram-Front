<template>
  <v-app dark>
    <v-navigation-drawer
      color="grey lighten-5"
      floating
      class="pa-4"
      app
      permanent
      v-model="drawer"
    >
      <v-layout class="pa-1">
        <div>
          <v-img
            width="130px"
            lazy-src="https://raw.githubusercontent.com/uzirthapa/instagram-clone/master/src/assets/instagram_logo.png"
            src="https://raw.githubusercontent.com/uzirthapa/instagram-clone/master/src/assets/instagram_logo.png"
          ></v-img>
        </div>
      </v-layout>
      <v-layout class="mt-10">
        <v-flex>
          <v-layout>
            <v-flex text-center>
              <v-avatar class="outlined" size="80">
                <v-avatar size="70">
                  <v-img
                    lazy-src="https://images.unsplash.com/photo-1554151228-14d9def656e4?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=633&q=80"
                    src="https://i.ibb.co/3T0Lvmx/23.jpg"
                  />
                </v-avatar>
              </v-avatar>
              <div class="mt-4 title">Vintetrois</div>
              <div class="mt-1 subtitle-2 grey--text">Amsterdam</div>
              <div class="mt-5">
                <v-layout>
                  <v-flex>
                    <div class="subtitle-2">Post</div>
                    <div class="subtitle-2 grey--text">116</div>
                  </v-flex>
                  <v-flex>
                    <div class="subtitle-2">Followers</div>
                    <div class="subtitle-2 grey--text">48m</div>
                  </v-flex>
                  <v-flex>
                    <div class="subtitle-2">Following</div>
                    <div class="subtitle-2 grey--text">48m</div>
                  </v-flex>
                </v-layout>
              </div>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
      <v-list
        nav
        dense
        class="mt-10"
      >
        <v-list-item-group
          active-class="#E7596F--text"
        >
          <v-list-item v-for="item in items">
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      flat
      app
      clipped-right
      color="white"
      clipped
    >
      <div class="d-flex align-center">
        <v-card color="grey lighten-4" outlined width="300px" class="pa-2 ml-4">
          <v-layout>
            <v-flex>
              <v-icon color="grey">mdi-magnify</v-icon>
              <span class="ml-2 grey--text">Search</span>
            </v-flex>
            <v-flex class="text-right">
              <v-icon color="grey">mdi-microphone-outline</v-icon>
            </v-flex>
          </v-layout>
        </v-card>
      </div>
      <v-spacer/>
      <v-btn
        color="pink accent-3"
        class="ma-2 white--text text-none"
      >
        <v-icon
          left
        >
          mdi-plus
        </v-icon>
        Create New Post
      </v-btn>
      <v-btn
        icon
        color="grey"
      >
        <v-icon>
          mdi-heart-outline
        </v-icon>
      </v-btn>
      <v-btn
        icon
        color="grey"
      >
        <v-icon>
          mdi-email-outline
        </v-icon>
      </v-btn>
      <v-avatar
        size="30"
      >
        <img
          src="https://media-exp1.licdn.com/dms/image/C4D03AQFBizn8RyO64A/profile-displayphoto-shrink_100_100/0/1618924385153?e=1643241600&v=beta&t=M1uxCBDOo0AnFObYDaZRF_h32xlPzR5yd3fzheMnzbU"
          alt="Gaby"
        >
      </v-avatar>
      <v-icon>mdi-menu-down</v-icon>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt/>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      items: [
        {
          icon: 'mdi-home-outline',
          title: 'Feed',
          to: '/'
        },
        {
          icon: 'mdi-compass-outline',
          title: 'Explore',
          to: '/'
        },
        {
          icon: 'mdi-pound',
          title: 'Trending',
          to: '/'
        },
        {
          icon: 'mdi-check-decagram',
          title: 'Top Post',
          to: '/'
        },
        {
          icon: 'mdi-account-outline',
          title: 'People',
          to: '/'
        },
        {
          icon: 'mdi-bell-outline',
          title: 'Notification',
          to: '/'
        },
        {
          icon: 'mdi-send-outline',
          title: 'Direct',
          to: '/'
        },
        {
          icon: 'mdi-chart-pie',
          title: 'Status',
          to: '/'
        },
        {
          icon: 'mdi-cog-outline',
          title: 'Settings',
          to: '/'
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
    }
  }
}
</script>


<style>
.v-avatar.outlined {
  border: 2px solid #e7596f;
  background-color: transparent;
  border-radius: 50%;
  height: 100px;
  width: 100px;
}
</style>
