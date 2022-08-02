<template>
<div class="card w-72 bg-slate-700 shadow-xl border border-base-content ">
  <figure><img class="mask mask-hexagon" src="https://placeimg.com/400/225/arch" alt="Shoes" /></figure>
  <div class="card-body">
    <h2 class="card-title">
        {{ title }}
    </h2>
    <div v-html="body"/>
    <div class="card-actions justify-end">
      <button class="btn btn-primary">See Post</button>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'PostCard',
  props: ['title', 'body']

}
</script>