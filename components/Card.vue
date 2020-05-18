<template>
    <v-card
      max-width="400"
      class="mx-auto"
    >
        <v-container>
            <v-row dense>
                <v-col cols="12">

                    <v-card
                        :color="color"
                        :href="url"
                        target="_blank"
                        dark
                    >
                        <div class="d-flex flex-no-wrap justify-space-between">
                        <div>
                            <v-card-title
                            class="headline"
                            v-text="title"
                            ></v-card-title>

                            <v-card-subtitle v-text="artistName"></v-card-subtitle>
                        </div>

                        <v-avatar
                            class="ma-3"
                            size="125"
                            tile
                        >
                            <v-img :src="image"></v-img>
                        </v-avatar>
                        </div>
                    </v-card>

                </v-col>
            </v-row>
        </v-container>
    </v-card>
</template>

<script>
export default {
    props: ['title', 'image', 'artistName', 'url', 'color']
}
</script>

<style>

</style>