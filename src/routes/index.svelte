<script>
	import DropdownFb from '$lib/DropdownFb.svelte';
	import DropdownTui from '$lib/DropdownTui.svelte';
</script>

<div class="p-8 bg-slate-200 h-screen">
	<h1 class="font-serif mb-4 font-extrabold text-xl text-center text-green-700">
		Welcome to the ultimate FLOWBITE VS TAILWIND UI comparison
	</h1>
	<div class="grid md:grid-cols-2 grid-cols-1">
		<div class="p-4 m-4 flex-col bg-white rounded-xl shadow-md">
			<header class="font-bold text-lg text-center text-black">Flowbite</header>
			<section class="bg-slate-200 rounded-lg m-2 p-2">
				<h1 class="font-semibold">Requirements:</h1>
				<a
					class="hover:text-blue-600"
					href="https://flowbite.com/docs/getting-started/introduction/#require-via-npm"
					>Check them Here!</a
				><br />
				They were too difficult to install so the javascript functionalities are out of the question
			</section>
			<h1 class="mt-8 font-semibold">Dropdown With No Wrapping DIV</h1>
			<DropdownFb />

			<div>
				<span class="font-semibold"> <pre> Logic:</pre></span>
				First I had to remove the built in js classes and the hidden property from the class
				<span> <pre> let showDropdown = false;</pre></span>
				<span> <pre> on:click= () => (showDropdown = !showDropdown)</pre></span>
			</div>

			<h1 class="mt-8 font-semibold">Wrapped in flex row justify justify-between</h1>
			<div class="flex flex-row justify-between bg-slate-200 p-2 m-2 rounded-lg">
				<div class="flex"><h1 class="font-semibold my-auto">Lorem ipsum</h1></div>
				<div class="flex">
					<DropdownFb />
				</div>
			</div>
		</div>
		<div class="p-4 m-4 flex-col bg-white rounded-xl shadow-md">
			<header class="font-bold text-lg text-center text-black">TailwindUI</header>
			<section class="bg-slate-200 rounded-lg m-2 p-1">
				<h1 class="font-semibold">Requirements:</h1>
				None
			</section>
			<h1 class="mt-8 font-semibold">Dropdown With No Wrapping DIV</h1>
			<DropdownTui />
			<div>
				<span class="font-semibold"> <pre> Logic:</pre></span>
				<span> <pre> let showDropdown = false;</pre></span>
				<span> <pre> on:click= () => (showDropdown = !showDropdown)</pre></span>
			</div>
			<h1 class="mt-8 font-semibold">Wrapped in flex row justify justify-between</h1>
			<div class="flex flex-row justify-between bg-slate-200 p-2 m-2 rounded-lg">
				<div class="flex">
					<h1 class="font-semibold my-auto">Lorem ipsum</h1>
				</div>
				<div class="flex">
					<DropdownTui />
				</div>
			</div>
		</div>
	</div>
</div>
