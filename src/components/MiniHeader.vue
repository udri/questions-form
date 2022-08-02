<template>
  <div id="miniHeader">
    <img alt="Vue logo" src="../assets/logo.png" width="50px" />
    <span>this is where the questions list will be</span>
  </div>
</template>

<script>
export default {};
</script>
<style>
#miniHeader {
  display: flex;
  flex-direction: row;
  align-content: center;
  align-items: center;
  justify-content: flex-start;
  flex-wrap: nowrap;
}
div#miniHeader * {
  margin: 20px;
}
</style>