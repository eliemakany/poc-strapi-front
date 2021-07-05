<template>
  <section class="py-5" style="background-color:#021A5C;">
    <div class="container">
      <div class="text-center text-white">
        <p class="display-6">{{content.title3Col}}</p>
        <p class="lead"><strong>{{content.baseline}}</strong></p>
      </div>
      <div class="row" style="color:#021A5C;">
        <div class="col bg-white rounded m-2 p-4">
          {{content.blocTextLeft}}
        </div>
        <div class="col bg-white rounded m-2 p-4">
          {{content.blockTextMiddle}}
        </div>
        <div class="col bg-white rounded m-2 p-4">
          {{content.blockTextRight}}
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ThreeCols",
  props: {
    content: Object
  }
}
</script>

<style scoped>

</style>