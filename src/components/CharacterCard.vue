<script>
export default {
    props: {
        characterData: Object,
    }
}
</script>
<template>
    <div class="card">
        <img :src="characterData.card_images[0].image_url" :alt="characterData.name">
        <h2 class="name">
            {{ characterData.name }}
        </h2>
        <div class="archetype">
            {{ characterData.archetype }}
        </div>
    </div>
</template>
<style lang="scss" scoped> 

.card{
    display: flex;
    flex-direction: column;
    

    
}
img {
    height: 90%;
    width: 90%;
    display: flex;
    margin: auto;
}
.name {
    margin:auto;
    background-color: orange;
    
}
.archetype {
    margin:auto;
    font-size: 30px;
    background-color: orange;
    
}

</style>