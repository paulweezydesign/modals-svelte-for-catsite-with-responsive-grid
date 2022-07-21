<script>
	export let modalContent;
</script>

<div on:click|self class='modal'>
	<div class='content'>
		<svelte:component on:click this={modalContent}/>
	</div>
</div>

<style>
	.modal {
		background-color: rgba(0, 0, 0, 0.4);
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		width: 100vw;
		height: 100vh;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	
	.content {
		background-color: white;
		width: 25em;
		min-height: 38em;
		
	}
</style>