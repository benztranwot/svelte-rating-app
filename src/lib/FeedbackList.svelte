<script>
  import { FeedbackStore } from "../stores";
  import { scale, fade } from "svelte/transition";
  import FeedbackItem from "./FeedbackItem.svelte";
</script>

{#each $FeedbackStore as feadback (feadback.id)}
  <div in:fade out:scale>
    <FeedbackItem item={feadback} />
  </div>
{/each}
