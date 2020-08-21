<template>
    <div>
        {{ beer }}
    </div>
</template>

<script>
    export default {
        name: 'User',
        props: {
            
        },
        data() {
            return {
              beer: {}
            }
        },
        created() {
            let url = "https://api.punkapi.com/v2/beers/"+this.$route.params.id
            
            this.$axios.get(url)
            .then(response => {
                this.beer = response.data[0]
            })
        },
        methods: {
            
        },
        components: {
            
        },
    }
</script>

<style scoped>
    
</style>