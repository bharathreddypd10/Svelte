<script>
	import Package from './Package.svelte';
	import Header from './Header.svelte';
	import Runes from './Runes.svelte';
	let count=0;

	const pkg = {
		name: 'svelte',
		version: 5,
		description: 'blazing fast',
		website: 'https://svelte.dev'
	};

</script>

<Header name="World"></Header>
<div>
	<Runes/>
</div>


<button onclick={()=>count++}>
	count is {count}
</button>

<Package {...pkg}/>

<style>
	div{
		margin-bottom: 10px;
		font-size: 10px;
	}
</style>

