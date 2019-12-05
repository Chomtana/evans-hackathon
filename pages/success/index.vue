
  
<template>
    <v-container >
        <v-flex Align="start" Justify="center">
            <img 
                src="@/static/red-check.png" 
                style="max-width: 100;
                    max-height: 60%;
                    height: 100%;
                    width: 100%;
                    object-fit: contain;"
            />
            <h2 align="center">Complete</h2>
        </v-flex>
    </v-container>
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
