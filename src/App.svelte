<script lang="ts">
  let red = 0
  let black = 0

  $: percentRed = red * 100 / (red + black)
  $: percentBlack = black * 100 / (red + black)
</script>

<main class="max-w-lg mx-auto py-6">
<div class="grid grid-cols-2 gap-8">
  <button class="bg-gray-200 ring-2 ring-offset-2 rounded-md ring-gray-400 py-4" on:click={() => {
    red = red + 1
  }}>
    <div class="bg-red-700 w-12 h-12 rounded-full mx-auto" />
    <h1 class="font-bold py-2">Red</h1>
    <span class="font-mono">{red} ({percentRed.toFixed(2)}%)</span>
  </button>
  <button class="bg-gray-200 ring-2 ring-offset-2 rounded-md ring-gray-400 py-4" on:click={() => {
    black = black + 1
  }}>
    <div class="bg-black w-12 h-12 rounded-full mx-auto" />
    <h1 class="font-bold py-2">Black</h1>
    <span class="font-mono">{black} ({percentBlack.toFixed(2)}%)</span>
  </button>
</div>
</main>
