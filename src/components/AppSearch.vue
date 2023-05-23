<script>
export default {
    data(){
        return {
            searchStr: "",
        };
    }
}
</script>
<template lang="">
    <div class="search-bar">
        <input type="text" placeholder="Search Card" v-model="searchStr">
        <select name="" id="">
            <option value="0">select status</option>
        </select>
        <button @click="$emit('performSearch', searchStr)">Search</button>
        <button>Reset</button>
    </div>
</template>
<style lang="scss" scoped>
    .search-bar {
        display: flex;
        justify-content: center;
        padding:20px 0;
        gap: 10px;
    }
</style>