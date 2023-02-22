<template>
  <div class="modal" v-if="showBlock" @click="stopTimer">
    <h1>Click to end game ...</h1>
  </div>
</template>

<script>
export default {
    props: ['delay'],

    data() {
        return {
            showBlock: false,
            timeTaken: 0,
            timer: null,
        }
    },

    mounted(){
        setTimeout(() => {
            this.showBlock = true;
            this.startTimer();
        }, this.delay)
    },
    methods: {
        startTimer(){
            this.timer = setInterval(() => {
                this.timeTaken += 10
            },10)
        },
        stopTimer(){
            clearInterval(this.timer)
            this.$emit('end', this.timeTaken)
        },
    },

}

</script>

<style>

.modal {
    width: 400px;
    background: rgb(12, 165, 12);
    font-weight: bold;
    margin: 80px auto;
    padding: 2rem;
    border-radius: 10px;
    
}

</style>