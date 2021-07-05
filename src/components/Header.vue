<style scoped>

.slogan {
    --slogan-url: url(https://storage.googleapis.com/q-oap-oaportal-assets/5fd371710a1082001b05cf20-bg-OAP-1920x588_10.jpg);
    background-image: linear-gradient(90deg,rgba(0,26,92,.8) 5%,rgba(0,26,92,0) 85%),linear-gradient(90deg,rgba(23,162,184,.4),rgba(23,162,184,.05)),var(--slogan-url); 
}
</style>

<template>
    <section class="py-5 slogan" style="background-size:cover;">
        <div class="container text-center">
            <div class="row py-lg-5">
            <div class="col-lg-6 col-md-8 mx-auto">
                <h1 class="fw-light text-white">{{content.title}}</h1>
                <p class="lead text-white">{{content.baseline}}</p>
                <p>
                <a :href="content.ctaLink" class="btn btn-primary my-2 mx-2">{{content.ctaText}}</a>
                <a href="#" class="btn btn-secondary my-2 mx-2">Secondary action</a>
                </p>
            </div>
        </div>
        </div>
  </section>
</template>

<script>
export default {
  props: {
    content: Object
  }
}
</script>