<script>
	import Modal from './Modal.svelte'
	import Component1 from './Component1.svelte'
	import Component2 from './Component2.svelte'
	import Component3 from './Component3.svelte'
	import Component4 from './Component4.svelte'
	// initialise modal state and content
	let showModal = false;
	let modalContent;
	
	// pass in component as parameter and toggle modal state
	function toggleModal(component) {
		modalContent = component;
		showModal = !showModal;
	}
	
</script>
<svelte:head>
	<script src="https://cdn.tailwindcss.com"></script>
</svelte:head>
<section> 
<main class="container mx-auto w-[100vw] flex flex-row space-x-4">


<button class="bg-transparent" on:click={() => (toggleModal(Component1))}>
<div class="max-w-xs mx-auto overflow-hidden bg-white will-change-contents hover:scale-105 rounded-lg shadow-black/40 shadow-lg dark:bg-gray-800">
 <img class="object-cover w-full h-56" src="https://images.unsplash.com/photo-1542156822-6924d1a71ace?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60" alt="avatar">
	<div class="py-5 text-center">
            <a href="#" class="block text-2xl font-bold text-gray-800 dark:text-white">John Doe</a>
            <span class="text-sm text-gray-700 dark:text-gray-200">Software Engineer</span>
        </div>
	</div>
</button>

<button on:click={() => (toggleModal(Component2))}>
<div class="max-w-xs mx-auto overflow-hidden bg-white will-change-contents hover:scale-105 rounded-lg shadow-black/40 shadow-lg dark:bg-gray-800">
 <img class="object-cover w-full h-56" src="https://images.unsplash.com/photo-1542156822-6924d1a71ace?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60" alt="avatar">
	<div class="py-5 text-center">
            <a href="#" class="block text-2xl font-bold text-gray-800 dark:text-white">John Doe</a>
            <span class="text-sm text-gray-700 dark:text-gray-200">Software Engineer</span>
        </div>
	</div>
</button>
<button on:click={() => (toggleModal(Component3))}>
 <div class="max-w-xs mx-auto overflow-hidden bg-white will-change-contents hover:scale-105 rounded-lg shadow-black/40 shadow-lg dark:bg-gray-800">
        <img class="object-cover w-full h-56" src="https://images.unsplash.com/photo-1542156822-6924d1a71ace?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60" alt="avatar">
        
        <div class="py-5 text-center">
            <a href="#" class="block text-2xl font-bold text-gray-800 dark:text-white">John Doe</a>
            <span class="text-sm text-gray-700 dark:text-gray-200">Software Engineer</span>
        </div>
    </div>
</button>
<button on:click={() => (toggleModal(Component4))}>
<div class="max-w-xs mx-auto overflow-hidden bg-white will-change-contents hover:scale-105 rounded-lg shadow-black/40 shadow-lg dark:bg-gray-800">
 <img class="object-cover w-full h-56" src="https://images.unsplash.com/photo-1542156822-6924d1a71ace?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60" alt="avatar">
	<div class="py-5 text-center">
            <a href="#" class="block text-2xl font-bold text-gray-800 dark:text-white">John Doe</a>
            <span class="text-sm text-gray-700 dark:text-gray-200">Software Engineer</span>
        </div>
	</div>
</button>
</main>
</section>
{#if showModal}
	<Modal on:click={toggleModal} {modalContent} />
{/if}
<style>
section {
	width: 100vw;
	height: 100vh;

}
main {
	display: flex;
	justify-content: center;
}
</style>