
  
<template>
    <v-card
      :loading="loading"
      color="#FF0000"
    >
         <img 
                src="@/static/effy.jpg" 
                style="max-width: 100%;
                    max-height: 30%;
                    height: 40%;
                    width: 100%;
                    object-fit: contain;"
            />
  
      <v-card-title>Arrived</v-card-title>
  
      <v-card-text>
        <v-row
          align="center"
          class="mx-0"
        >
          <v-rating
            :value="3.5"
            color="amber"
            dense
            half-increments
            readonly
            size="14"
          ></v-rating>
  
        </v-row>
    
        <v-card-title>Driver : Nattakit kundam</v-card-title>
        <div>License : FF01ET</div>
        <div>Route : Rama4 - Chula</div>
      </v-card-text>
  
      <v-divider class="mx-4"></v-divider>
  
      <v-card-title>Comment</v-card-title>
      <v-card-text>
        <v-textarea
            background-color="grey lighten-2"
            color="black"
        ></v-textarea>
       <v-card-actions>
        <v-btn
          color="White"
          text
          @click="reserve"
        >
          Send
        </v-btn>
      </v-card-actions>

      </v-card-text>
    </v-card>
</template>

<script>
export default {
    name: "Success",
    components: {
    },
    data() {
        return {
        };
    },
    methods: {
    }
};
</script>
