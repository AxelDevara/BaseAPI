<script lang="ts">
  export let text: String;
  export let badge: String = "";
</script>

<div class="flex flex-row items-center gap-3">
    <h2 class="mt-4 h3 mb-3">{text}</h2>
    {#if badge.length > 0}
    <span class="badge py-2 h-6 rounded-full variant-filled">{badge}</span>
    {/if}
</div>
<hr />
