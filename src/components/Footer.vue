<template>
  <div class="footer">
    <p>SOFIA BERGLUND</p>
    <p>berglund.sofia@gmail.com</p>
    <p>073-650 84 80</p>
  </div>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style lang="scss">
.footer {
  background-color: #f6a623;
  text-align: center;
  color: white;
  height: 100px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  p {
    margin: 0;
    font-size: 14px;
  }
}
</style>