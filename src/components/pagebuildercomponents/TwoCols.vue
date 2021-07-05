<template>
  <section class="py-5">
    <div class="container">
      <div class="row">
        <div class="col">
          <p class="display-6">{{content.title2Col}}</p>
          <p class="lead">{{content.baseline}}</p>
          <div>
            {{content.blocTextLeft}}
          </div>
        </div>
        <div class="col">
          <div>
            {{content.blocTextRight}}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "TwoCols",
  props: {
    content: Object
  }
}
</script>

<style scoped>

</style>