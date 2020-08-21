<template>
    <div>
        <form action="">
            <label for="">Nom:</label>
            <input type="text" v-model="nom">
            <br>
            <label for="">Email:</label>
            <input type="email" v-model="email">
            <br>
            <label for="">Message</label>
            <br>
            <textarea name="" id="" cols="30" rows="10" v-model="message"></textarea>
            <button @click.prevent="contact">OK</button>
        </form>

       <router-link class="button" to="/">Home</router-link>
    </div>
</template>

<script>
    export default {
        name: 'formulaire',
        props: {
            
        },
        data() {
            return {
                nom: "",
                email: "",
                message: ""
            }
        },
        methods: {
            contact() {
                this.$emit("qui", this.nom)
                this.$router.push({name:'Home'})
                //this.$router.go(-1)
            }
        }
    }
</script>

<style scoped>
    
</style> 