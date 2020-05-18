<template>
  <div>
      <h3>Result for {{$route.params.id}}</h3>
      <div v-if="albumExists">
        <div v-for="(album, index) in albumData">
          <card
            :title="album.collectionName"
            :image="album.artworkUrl100"
            :artistName="album.artistName"
            :url="album.artistViewUrl"
            :color="picker(index)"
          ></card>
        </div>
      </div>
      <div v-else>
        <h1>Album Dons't Exist</h1>
      </div>
  </div>
</template>

<script>
import Card from '~/components/Card.vue';

export default {
  middleware: 'search',
  components:{
    'card': Card
  },
  data(){
    return {
      albumData: this.$store.state.albums
    }
  },
  methods:{
    picker(index){
      return index % 2 == 0 ? 'red': 'blue';
    }
  },
  computed: {
    albumExists(){
      return this.albumData.length > 0;
    }
  }
}
</script>

<style>

</style>