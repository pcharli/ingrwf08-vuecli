<template>
  <div class="contact">
    <h1>Contact</h1>
    <p>Texte</p>
    <formulaire @qui="$emit('qui', $event)"></formulaire>
  </div>
</template>
<script>
import formulaire from "@/components/Formulaire.vue"

export default {
  name: "contact",
  components: {
    formulaire
    }
}
</script>
<style lang="scss" scoped>
    h1{
        color: $titre;
    }
</style>