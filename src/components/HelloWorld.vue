<template>
<div>
  <v-carousel hide-delimiters class="content" style="margin-top:8%">
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    >
    <v-row
            class="fill-height"
            align="center"
            justify="center"
          >
            <div class="display-4 white--text">{{item.text}}</div>
          </v-row>
    </v-carousel-item>
  </v-carousel>
  <div>
    <v-flex xs6 sm6 md12 xl12>
        <v-row
            align="center"
            justify="center"
            class="ma-5 mx-auto">
            <v-col cols="12" xs="12" sm="12" md="3" lg="3" xl="3" v-for="(something,m) in category" :key="m"
            align="center"
            justify="center"
            class="ma-4">
          <v-card
           align="start"
          justify="space-around"
          :elevation= "3"
            v-for="(category,n) in something"
            :key="n"
            class="ma-4 mx-6"
            max-width="600"
            min-width="300"
            outlined
            tile
          >
    <v-img
      class="white--text align-end"
      height="200px"
      :src= "category.src"
    >
      <v-card-title>{{category.cat}}</v-card-title>
    </v-img>

    <v-card-text class="text--primary">
      <div>{{category.description}}</div>
    </v-card-text>

    <v-card-actions>
      <v-btn
        color="orange"
        text
      >
        Explore
      </v-btn>
    </v-card-actions>
    </v-card>
    </v-col>
    </v-row>
  </v-flex>
  </div>
</div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          text: 'Action',
          src: 'https://images.unsplash.com/photo-1520371764250-8213f40bc3ed?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=967&q=80'
        },
        {
          text: 'SciFi',
          src: 'https://images.unsplash.com/photo-1457979406492-d1e6b97f3f55?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80'
        },
        {
          text: 'History',
          src: 'https://images.unsplash.com/photo-1447422285000-7b54b1969b7b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80'
        },
        {
          text: 'Science',
          src: 'https://images.unsplash.com/photo-1518152006812-edab29b069ac?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80'
        }
      ],
      category: [
        [
          { cat: 'Action',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
            src: 'https://images.unsplash.com/photo-1520371764250-8213f40bc3ed?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=967&q=80' },
          { cat: 'Drama',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
            src: 'https://images.unsplash.com/photo-1539964604210-db87088e0c2c?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1052&q=80' },
          { cat: 'Fiction',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
            src: 'https://images.unsplash.com/photo-1533991177543-e1ac3b4ba42e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1055&q=80' }
        ],
        [
          { cat: 'Adventure',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
            src: 'https://images.unsplash.com/photo-1483444308400-fb9510501d23?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1053&q=80' },
          { cat: 'Historical',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
            src: 'https://images.unsplash.com/photo-1447422285000-7b54b1969b7b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80' },
          { cat: 'Science Fiction',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
            src: 'https://images.unsplash.com/photo-1457979406492-d1e6b97f3f55?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80' }
        ],
        [
          { cat: 'Nonfiction',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
            src: 'https://images.unsplash.com/photo-1501413993417-48a2d962ed54?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80' },
          { cat: 'Romance',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
            src: 'https://images.unsplash.com/reserve/Af0sF2OS5S5gatqrKzVP_Silhoutte.jpg?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80' },
          { cat: 'Science',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
            src: 'https://images.unsplash.com/photo-1518152006812-edab29b069ac?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80' }
        ]
      ]
    }
  }
}
</script>
