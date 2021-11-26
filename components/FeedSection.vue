<template>
  <div class="mt-10">
    <v-row>
      <v-col>
        <div class="title">Latest Feed</div>
      </v-col>
      <v-spacer/>
      <v-btn icon depressed class="text-none" color="grey">
        <v-icon>mdi-menu</v-icon>
      </v-btn>
      <v-btn icon depressed class="text-none" color="pink accent-3">
        <v-icon>mdi-view-grid-outline</v-icon>
      </v-btn>
    </v-row>
    <v-row class="mt-5">
      <v-col v-for="(post, i) in posts" :key="i">
        <v-card
          elevation="12"
          height="230"
          width="242"
          color="blue"
          class="mr-4"
        >
          <v-img
            height="230"
            :src="post.src"
          />
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        {
          src: 'https://images.unsplash.com/photo-1525138079-9424be9df411?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=675&q=80'
        },
        {
          src: 'https://images.unsplash.com/photo-1523224949444-170258978eef?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=564&q=80'
        },
        {
          src: 'https://images.unsplash.com/photo-1551818633-579bccc6210c?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1267&q=80'
        },
        {
          src: 'https://images.unsplash.com/photo-1478296046035-d4fc77bec472?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80'
        },
        {
          src: 'https://images.unsplash.com/photo-1525138079-9424be9df411?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=675&q=80'
        },
        {
          src: 'https://images.unsplash.com/photo-1523224949444-170258978eef?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=564&q=80'
        },
      ],
    }
  }
}
</script>
