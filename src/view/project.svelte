<script>
	import projects from '../Json/Project.json';
	import { Icon } from 'svelte-icons-pack';
	import { BsGithub } from 'svelte-icons-pack/bs';
	import { FiExternalLink } from 'svelte-icons-pack/fi';
</script>

<div class="flex h-[85vh] w-full max-w-7xl flex-col rounded-md bg-white p-7 shadow-xl">
	<h1 class="mb-5 text-3xl font-bold text-black">My Projects</h1>
	<div class="flex-1 overflow-y-auto pr-4">
		<div class="grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
			{#each projects as project}
				<div class="flex flex-col overflow-hidden rounded-lg border bg-gray-50 shadow-sm transition-shadow duration-300 hover:shadow-lg">
					<img src={`/${project.image}`} alt={project.title} class="h-48 w-full object-cover" />
					<div class="flex flex-grow flex-col p-4">
						<h2 class="text-xl font-bold text-black">{project.title}</h2>
						<p class="text-sm text-gray-500">{project.year}</p>
						<p class="mt-2 flex-grow text-gray-700">{project.description}</p>
						<div class="mt-4 flex flex-wrap gap-2">
							{#each project.languages as lang}
								<span class="rounded-full bg-gray-200 px-3 py-1 text-xs font-semibold text-gray-800">{lang}</span>
							{/each}
						</div>
						<div class="mt-auto flex items-center gap-4 pt-4">
							{#if project.link.source_code}
								<a href={project.link.source_code} target="_blank" rel="noopener noreferrer" class="text-gray-600 hover:text-black" aria-label="Source Code">
									<Icon src={BsGithub} size="24" />
								</a>
							{/if}
							{#if project.link.website}
								<a href={project.link.website} target="_blank" rel="noopener noreferrer" class="text-gray-600 hover:text-black" aria-label="Live Website">
									<Icon src={FiExternalLink} size="24" />
								</a>
							{/if}
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</div>