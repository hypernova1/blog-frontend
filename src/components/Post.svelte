<script>
  export let post = {};
  const localPost = post;
</script>
<style>
  li {
      list-style-type: none;
  }
</style>
<li>
  <section>
    <h1>{localPost.title}</h1>
    {localPost.writer}
  </section>
</li>
