<script>
	let name = 'Gugu';
	let age = 24;

	$: uppercaseName = name.toUpperCase();
	$: console.log(name)
	$: if (name === "Gugu") {
		age = 33
	}

	function incrementAge() {
		age += 1
	}
	function changeName() {
		name = "GPLOVE"
	}

	function nameInput (event) {
		name = event.target.value
	}

</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {age}!</h1>
<h2>{uppercaseName}</h2>
<button on:click={incrementAge}>Change Age</button>
<button on:click={changeName}>Change Name</button>
<!--<input type="text" value="{name}" on:input={nameInput}>-->
<input type="text" bind:value={name}>
