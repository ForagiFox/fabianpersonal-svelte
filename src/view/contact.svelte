<script>
	import { BsGithub,BsLinkedin } from 'svelte-icons-pack/bs';
	import { Icon } from 'svelte-icons-pack';
</script>

<div class="bg-white shadow-xl w-full lg:w-1/2 mt-9 lg:mt-0 rounded-md">
	<div class="py-4 px-7">
		<h1 class="text-3xl font-bold mb-5 text-black">
			Connect Me
		</h1>
		<div class="mb-5">
                <p class="text-black font-semibold mb-1">Email</p>
                <p class="text-black font-semibold">fabianananda0912@gmail.com</p>
            </div>
		<p class="text-black font-semibold mb-1">Connect me</p>
		<div class="flex gap-3">
			<a href="https://github.com/KnoyanMitsu"><Icon size="40" src={BsGithub} /></a>
			<a href="https://www.linkedin.com/in/fabian-ananda-merdana-400551228/"><Icon size="40" src={BsLinkedin} /></a>
		</div>
	</div>
</div>
