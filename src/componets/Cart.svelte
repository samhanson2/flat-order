<script>
	let foodItems = [];
	function addItem() {
		foodItems = [...foodItems, ''];
	}
	function removeItem(index) {
		foodItems = [...foodItems.slice(0, index), ...foodItems.slice(index+1)];
	}
</script>
{#each foodItems as Item, index}
	<input bind:value={foodItems[index]}>
	<button on:click={()=>removeItem(index)}>Delete</button>
  <br>
{/each}
<button on:click={addItem}>Add</button>