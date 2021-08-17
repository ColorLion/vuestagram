<template>
  <div class="list">
    <v-container fluid class="mt-4">
    <v-row>
      <v-col cols="12">
        <template>
          <v-toolbar
            color="#23262D"
            dark
          >
            <v-toolbar-title>D20</v-toolbar-title>
            <v-spacer></v-spacer>
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
                
                <!-- card 실험 -->
                <template>
                  <v-row>
                    <v-col cols="12" sm="4">
                      <v-card
                        class="mx-auto"
                        outlined
                      >
                        <v-list-item three-line>
                          <v-list-item-content>
                            <div class="text-overline mb-4">
                              OVERLINE
                            </div>
                            <v-list-item-title class="text-h5 mb-1">
                              Headline 5
                            </v-list-item-title>
                            <v-list-item-subtitle>Greyhound divisely hello coldly fonwderfully</v-list-item-subtitle>
                          </v-list-item-content>

                          <v-list-item-avatar
                            tile
                            size="80"
                            color="grey"
                          ></v-list-item-avatar>
                        </v-list-item>
                        <v-card-actions>
                          <v-btn
                            outlined
                            rounded
                            text
                          >
                            Button
                          </v-btn>
                        </v-card-actions>
                      </v-card>
                    </v-col>
                  </v-row>
                </template>

                <v-row>
                  <v-col cols="12" sm="4" v-for="child in item.items" :key="child.title" class="title">
                    <v-list-item-content>
                      <v-list-item-title v-text="child.title"></v-list-item-title>
                      <!--<v-img :src="child.src" aspect-ratio="1.75"></v-img>-->
                      <v-img contain :src="child.src"></v-img>
                      <v-rating v-model="child.rating" background-color="pink lighten-3" color="pink"></v-rating>
                    </v-list-item-content>
                  </v-col>
                </v-row>

                <v-list-item
                  v-for="child in item.items"
                  :key="child.title"
                  class="title"
                >
                  <v-list-item-content>
                    <v-list-item-title v-text="child.title"></v-list-item-title>
                    <!--<v-img :src="child.src" aspect-ratio="1.75"></v-img>-->
                    <v-img contain :src="child.src"></v-img>
                    <v-rating v-model="child.rating" background-color="pink lighten-3" color="pink"></v-rating>
                  </v-list-item-content>
                </v-list-item>

                <v-list-item
                  v-for="child in item.items"
                  :key="child.title"
                  class="title"
                >
                  <v-list-item-content>
                    <template>
                      <v-row>
                        <v-col cols="12" sm="4">
                          <v-card
                            class="mx-auto"
                            outlined
                            
                          >
                            <v-list-item three-line>
                              <v-list-item-content>
                                <div class="text-overline mb-4">
                                  OVERLINE
                                </div>
                                <v-list-item-title class="text-h5 mb-1">
                                  Headline 5
                                </v-list-item-title>
                                <v-list-item-subtitle>Greyhound divisely hello coldly fonwderfully</v-list-item-subtitle>
                              </v-list-item-content>

                              <v-list-item-avatar
                                tile
                                size="80"
                                color="grey"
                              ></v-list-item-avatar>
                            </v-list-item>
                            <v-card-actions>
                              <v-btn
                                outlined
                                rounded
                                text
                              >
                                Button
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-col>
                        <v-col cols="12" sm="4">
                          <v-card
                            class="mx-auto"
                            outlined
                            
                          >
                            <v-list-item three-line>
                              <v-list-item-content>
                                <div class="text-overline mb-4">
                                  OVERLINE
                                </div>
                                <v-list-item-title class="text-h5 mb-1">
                                  Headline 5
                                </v-list-item-title>
                                <v-list-item-subtitle>Greyhound divisely hello coldly fonwderfully</v-list-item-subtitle>
                              </v-list-item-content>

                              <v-list-item-avatar
                                tile
                                size="80"
                                color="grey"
                              ></v-list-item-avatar>
                            </v-list-item>
                            <v-card-actions>
                              <v-btn
                                outlined
                                rounded
                                text
                              >
                                Button
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </v-col>
                      </v-row>
                    </template>
                  </v-list-item-content>
                </v-list-item>
            </v-list-group>
          </v-list>
        </template>
      </v-col>
    </v-row>
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
          title: '최상',
          items: [{ title: 'List Item', src: 'https://picsum.photos/400/300?image=1', rating: 0,}],
          
        },
        {
          action: 'mdi-silverware-fork-knife',
          title: '상',
          //active: true,
          items: [
            { title: 'Breakfast & brunch', src: 'https://picsum.photos/400/300?image=2', rating: 0,},
            { title: 'New American', src: 'https://picsum.photos/400/300?image=3', rating: 0,},
            { title: 'Sushi', src: 'https://picsum.photos/400/300?image=4', rating: 0,},
          ],
          
        },
        {
          action: 'mdi-school',
          title: '중상',
          items: [{ title: 'List Item', src: 'https://picsum.photos/400/300?image=5', rating: 0,}],
          
        },
        {
          action: 'mdi-run',
          title: '중',
          items: [{ title: 'List Item', src: 'https://picsum.photos/400/300?image=6', rating: 0,}],
          
        },
        {
          action: 'mdi-bottle-tonic-plus',
          title: '중하',
          items: [{ title: 'List Item', src: 'https://picsum.photos/400/300?image=7', rating: 0,}],
        },
        {
          action: 'mdi-content-cut',
          title: '하',
          items: [
            { title: 'What Happend', src: require('@/static/img/1120.png'), rating: 0,},
            { title: 'Lucid(PIU Edit)', src: require('@/static/img/1314.png'), rating: 0,},
            { title: 'Gargoyle', src: require('@/static/img/1121.png'), rating: 0,},
            { title: 'Cleaner', src: require('@/static/img/1101.png'), rating: 0,},
            ],
        },
        {
          action: 'mdi-tag',
          title: '종특',
          items: [{ title: 'List Item', src: 'https://picsum.photos/400/300?image=10', rating: 0,}],
          
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