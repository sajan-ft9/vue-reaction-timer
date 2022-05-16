<template>
  <p id="results">Reaction Time: {{ score }} ms</p>
  <p id="rank">{{ rank }}</p>
</template>

<script>
export default {
    props:['score'],
    data(){
        return {
            rank: null
        }
    },
    mounted(){
        if(this.score < 250){
            this.rank = "Ninja fingers"
        } else if (this.score < 400){
            this.rank = "Rapid Fingers"
        } else {
            this.rank = "Snail Pace..."
        }
    }
}
</script>

<style>
#results{
    padding: 20px;
    }
#rank{
    color: rgb(41, 230, 167);
    font-weight: bold;
}
</style>