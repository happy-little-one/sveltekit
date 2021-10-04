<script context="module">
export async function load() {
  return {
    props: {
      text: Math.random(),
    },
  }
}
</script>

<script>
import { goto } from '$app/navigation'
export let text
</script>

<h1>{text}</h1>

<button on:click={() => goto(`/news/${Math.floor(Math.random() * 100)}`)}>test</button>
