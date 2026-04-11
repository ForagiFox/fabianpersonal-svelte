<script>
	import Navbar from './Navbar.svelte';
	import Title from './title.svelte';
	import About from './about.svelte';
	import Contact from './contact.svelte';
	import Project from './project.svelte';
</script>
<Navbar />
<div class="h-screen w-full overflow-y-scroll overflow-x-hidden scroll-smooth lg:snap-y lg:snap-mandatory">
	<Title />

	<section id="about" class="flex min-h-screen items-center justify-center bg-gray-50 p-4 lg:snap-start lg:p-8">
		<About />
	</section>

	<section id="projects" class="flex min-h-screen items-center justify-center bg-gray-100 p-4 lg:snap-start lg:p-8">
		<Project />
	</section>

	<section id="contact" class="flex min-h-screen items-center justify-center bg-gray-50 p-4 lg:snap-start lg:p-8">
		<Contact />
	</section>
</div>

