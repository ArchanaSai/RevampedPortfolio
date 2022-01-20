<script>
	import Age from './Age.svelte'
	let name = "Archana"
	let age = 30
	$: dogAge = age * 2
	
	function add(){
		age += 1	
	}
	
	function minus(){
		age -= 1
	}
	
</script>
<style>
h1{
		color: red;
	}
</style>
<h1>
	Hello {name}
</h1>
<Age {age}></Age>
<Age age= {dogAge} yearType="dog"></Age>

<button on:click={add}>
	+
</button>
<button on:click={minus}>
	-
</button>