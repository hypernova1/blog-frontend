<script>
  import { Button } from 'sveltestrap';
  export let post = {};
  const localPost = post;
</script>
<li>{localPost.title}<Button color="primary">확인</Button></li>