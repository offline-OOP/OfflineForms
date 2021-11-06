<template>
  <q-page class="flex flex-center">
    <iframe
      src="https://docs.google.com/forms/d/e/1FAIpQLScLpWrStAbP8INXqhMNq3HqGfDqgh7LtDlx4WEpZuoTda1g6Q/viewform?embedded=true"
      class="form" frameborder="0" marginheight="0" marginwidth="0"
    >
      Загрузка…
    </iframe>
  </q-page>
</template>

<script>
export default {
  name: "Organizers"
}
</script>

<style scoped>
.form {
  width: 100%;
  min-height: calc(100vh - 50px);
}
</style>
