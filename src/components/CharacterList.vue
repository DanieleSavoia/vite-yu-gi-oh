<script>
import CharacterCard from './CharacterCard.vue';
import { store } from "../store";
export default {
    data() {
        return {
            store,
        }
    },
    components: {
        CharacterCard,
    }
}
</script>
<template lang="">
    <CharacterCard v-for="character in store.characterList" :key="character.id"/>
    <CharacterCard/>
    <CharacterCard/>
</template>
<style lang="">
    
</style>