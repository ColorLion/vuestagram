<template>
  <div class="list">
    <v-container fluid class="mt-4">
      <template>
        <v-card
          class="mx-auto"
          max-width="500"
        >
        <v-toolbar
          color="teal"
          dark
        >
          <v-app-bar-nav-icon></v-app-bar-nav-icon>

          <v-toolbar-title>Topics</v-toolbar-title>

          <v-spacer></v-spacer>

          <v-btn icon>
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </v-toolbar>

          <v-list>
            <v-list-group
              v-for="item in items"
              :key="item.title"
              v-model="item.active"
              :prepend-icon="item.action"
              no-action
            >
              <template v-slot:activator>
                <v-list-item-content>
                  <v-list-item-title v-text="item.title"></v-list-item-title>
                </v-list-item-content>
              </template>

              <v-list-item
                v-for="child in item.items"
                :key="child.title"
              >
                <v-list-item-content>
                  <v-list-item-title v-text="child.title"></v-list-item-title>
                  <v-img :src="child.src" aspect-ratio="2" class="grey lighten-2"></v-img>
                  <v-rating v-model="child.rating" background-color="pink lighten-3" color="pink"></v-rating>
                </v-list-item-content>
              </v-list-item>
            </v-list-group>
          </v-list>
        </v-card>
      </template>
    </v-container>
  </div>
</template>

<script>
export default{
  name: 'list',
  data() {
    return {
      items: [
        {
          action: 'mdi-ticket',
          items: [{ title: 'List Item', src: 'https://picsum.photos/400/300?image=1', rating: 0,}],
          title: 'Attractions',
        },
        {
          action: 'mdi-silverware-fork-knife',
          //active: true,
          items: [
            { title: 'Breakfast & brunch', src: 'https://picsum.photos/400/300?image=2', rating: 0,},
            { title: 'New American', src: 'https://picsum.photos/400/300?image=3', rating: 0,},
            { title: 'Sushi', src: 'https://picsum.photos/400/300?image=4', rating: 0,},
          ],
          title: 'Dining',
        },
        {
          action: 'mdi-school',
          items: [{ title: 'List Item', src: 'https://picsum.photos/400/300?image=5', rating: 0,}],
          title: 'Education',
        },
        {
          action: 'mdi-run',
          items: [{ title: 'List Item', src: 'https://picsum.photos/400/300?image=6', rating: 0,}],
          title: 'Family',
        },
        {
          action: 'mdi-bottle-tonic-plus',
          items: [{ title: 'List Item', src: 'https://picsum.photos/400/300?image=7', rating: 0,}],
          title: 'Health',
        },
        {
          action: 'mdi-content-cut',
          items: [{ title: 'List Item', src: 'https://picsum.photos/400/300?image=8', rating: 0,}],
          title: 'Office',
        },
        {
          action: 'mdi-tag',
          items: [{ title: 'List Item', src: 'https://picsum.photos/400/300?image=10', rating: 0,}],
          title: 'Promotions',
        },
      ],
    }
  }
}
</script>
<style scoped>
  .datatab{
    background: #23252D !important;
  }
</style>