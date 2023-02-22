<template>
  <h1> You took {{ score }} ms to complete the game</h1>
  <h1>{{ this.rank }}</h1>
</template>

<script>
export default {
    props: ['score'],

    data() {
        return {
            rank: null,
        }
    },
    mounted() {
        if(this.score < 700){
            this.rank="Well done. You scored among the first percentile"
        }
        else if (this.score <1200){
            this.rank="Good work in getting to the 2nd percentile. You can better"
        }
        else {
            this.rank="Too slow. Please improve !!!"
        }
    }

}
</script>

<style>

</style>