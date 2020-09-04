<script>
  import axios from 'axios';
  import Post from '../components/Post.svelte';
  import { writable } from 'svelte/store';

  const posts = writable([]);
  let localPosts = [];

  posts.subscribe((value) => {
    localPosts = value;
  });
  axios.get("http://localhost:8080/v1/api/post")
    .then((res) => res.data)
    .then((data) => {
      posts.set(data);
  });
</script>
<ul>
  {#each localPosts as post}
    <Post post={post}/>
  {/each}
</ul>