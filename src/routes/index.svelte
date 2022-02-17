<script>
	import DropdownFb from '$lib/DropdownFb.svelte';
	import DropdownTui from '$lib/DropdownTui.svelte';
	import NavbarFb from '$lib/NavbarFb.svelte';
	import NavbarTui from '$lib/NavbarTui.svelte';
</script>

<div class="p-1 sm:p-2 lg:p-8 bg-slate-200 h-full">
	<header>
		<div class="flex justify-center">
			<a
				class="absolute top-8 left-8 "
				href="https://github.com/lorenzodonadio/flowbitevstailwindui"
			>
				<svg
					height="32"
					aria-hidden="true"
					viewBox="0 0 16 16"
					version="1.1"
					width="32"
					data-view-component="true"
					class="octicon octicon-mark-github v-align-middle rounded-full hover:bg-slate-50"
				>
					<path
						fill-rule="evenodd"
						d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"
					/>
				</svg>
			</a>

			<h1 class="mb-4 font-extrabold text-2xl text-center">
				Welcome to a Flowbite vs TailwindUI comparison
			</h1>
		</div>
		<h1 class="mb-4 font-bold text-lg text-center">
			Built with <a href="https://svelte.dev/">
				<span class="text-orange-700 hover:text-orange-500">Svelte</span>
			</a>
		</h1>
	</header>

	<div class="grid lg:grid-cols-2 grid-cols-1">
		<!-- Requirements Flowbite -->
		<div class="p-4 m-4 flex-col bg-white rounded-xl shadow-md">
			<header class="font-bold text-lg text-center text-black">Requirements Flowbite</header>
			<section class="bg-slate-200 rounded-lg m-2 p-2">
				<h1 class="font-semibold">
					Requirements: TailwindCSS +
					<a
						class="hover:text-blue-600"
						href="https://flowbite.com/docs/getting-started/introduction/#require-via-npm"
						>Flowbite.js</a
					>
				</h1>
				Flowbite was difficult to install and set up so the javascript functionalities are implemented
				in svelte.
			</section>
		</div>
		<!-- Requirements Tailwind ui -->
		<div class="p-4 m-4 flex-col bg-white rounded-xl shadow-md">
			<header class="font-bold text-lg text-center text-black">Requirements TailwindUI</header>
			<section class="bg-slate-200 rounded-lg m-2 p-1">
				<h1 class="font-semibold">Requirements: Only TailwindCSS</h1>
				So this comparison is only regarding css, again no out of the box javascript functionalities
				implemented.<br />
			</section>
			<span>*only the free components were compared</span>
		</div>
	</div>
	<!-- Tailwindui Navbar -->
	<div class="py-4 m-4 flex-col bg-white rounded-xl shadow-md">
		<header class="font-bold text-lg text-center text-black">Tailwind Navbar</header>
		<div class="px-4 my-2">
			<span class="font-semibold"> <pre> Logic:</pre></span>
			same as the dropdown, for the user info. and for the mobile menu
		</div>
		<NavbarTui />
	</div>
	<!-- Flowbite Navbar -->
	<div class="py-4 m-4 flex-col bg-white rounded-xl shadow-md">
		<header class="font-bold text-lg text-center text-black">Flowbite Navbar</header>
		<div class="px-4 my-2">
			<span class="font-semibold"> <pre> Logic:</pre></span>
			same as the dropdown, for the the mobile menu
		</div>
		<NavbarFb />
	</div>
	<div class="grid lg:grid-cols-2 grid-cols-1">
		<!-- Flowbite Dropdown -->
		<div class="p-4 m-4 flex-col bg-white rounded-xl shadow-md">
			<header class="font-bold text-lg text-center text-black">Flowbite Dropdown</header>

			<h1 class="mt-2 font-semibold">Dropdown With No Wrapping DIV</h1>
			<DropdownFb />

			<div>
				<span class="font-semibold"> <pre> Logic:</pre></span>
				First the built in js classes and the "hidden" property from the class
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
		<!-- TailwindUi Dropdown -->
		<div class="p-4 m-4 flex-col bg-white rounded-xl shadow-md">
			<header class="font-bold text-lg text-center text-black">TailwindUI Dropdown</header>

			<h1 class="mt-2 font-semibold">Dropdown With No Wrapping DIV</h1>
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
