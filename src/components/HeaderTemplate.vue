<template>

</template>

<script>
export default {
  name: "HeaderTemplate"
}
</script>

<style scoped>
  .header {
    display: flex;
    width: 100%;
    height: 100px;
    padding: 4em;
    justify-content: space-between;
    align-items: center;
    background : #00ADB5;
  }

  #logLinks {
    color: #EEEEEE;
    display: flex;
    justify-content: space-between;
    width: 20%;
  }

  #logLinks a {
    text-decoration: none;
    color: #EEEEEE;
  }
</style>