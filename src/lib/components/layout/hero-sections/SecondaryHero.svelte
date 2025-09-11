<script lang="ts">
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";

	let {
		title,
		subtitle,
		imageSrc = "https://www.unc.mn/image-placeholder.svg",
		...rest
	}: {
		title: string;
		subtitle: string;
		imageSrc: string;
		[key: string]: any;
	} = $props();
</script>

<header class="border-b border-gray-800 bg-gray-950" {...rest}>
	<div class="text-title3 section-px section-py container mx-auto grid gap-16 gap-y-0">
		<SectionHeader {title} {subtitle} size="lg" />
		<div class="aspect-video overflow-clip rounded-xl bg-gray-900 border border-gray-800">
			<img
				class="h-full w-full object-cover"
				src={imageSrc}
				alt="Team of data scientists and life sciences professionals collaborating"
			/>
		</div>
	</div>
</header>
