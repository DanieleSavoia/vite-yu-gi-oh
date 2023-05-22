<script>
import AppSearch from './components/AppSearch.vue';
import CharacterList from './components/CharacterList.vue';
import ResultsMessage from './components/ResultsMessage.vue';
import axios from "axios";
import { store } from "./store";
export default {
    data() {
        return {
            store,
        };

    },
    components: {
        AppSearch,
        CharacterList,
        ResultsMessage,
    },
    created () {
        // facciamo la richiesta qui api
        axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php")
        .then(response => (this.store.characterList = response.data.results));
    }
}
</script>
<template lang="">
    <h1>
        yu-gi-oh api
    </h1>
    <main>
        <AppSearch/>
        <CharacterList/>
        <ResultsMessage/>
    </main>
</template>
<style lang="scss">
    
</style>