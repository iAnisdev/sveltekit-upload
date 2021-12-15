<script>
	import Uploader from './components/uploader.svelte';
	
	function handleSingleUpload(event){
		console.log("handleSingleUpload returned url ==> ", event.detail)
	}
	
	function handleMultipleUpload(event) {
		console.log("handleMultipleUpload returned urls ==> ", event.detail)
	}

</script>

<main>
	<h1>Upload FIle To Imagegur!</h1>
	<p>Single File upload</p>
	<Uploader on:upload={handleSingleUpload}/>
	<p>Multiple File upload</p>
	<Uploader multiple={true} on:upload={handleMultipleUpload}/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>