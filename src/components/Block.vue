<template>
  <div class="modal">
    <h1>Click to end game ...{{ delay }}</h1>
  </div>
</template>

<script>
export default {
    props: ['delay']

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