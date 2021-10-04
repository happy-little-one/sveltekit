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

function on_next() {
  goto(`/news/${Math.floor(Math.random() * 100)}`)
}
</script>

<h1>{text}</h1>

<button on:click={on_next}>next</button>
