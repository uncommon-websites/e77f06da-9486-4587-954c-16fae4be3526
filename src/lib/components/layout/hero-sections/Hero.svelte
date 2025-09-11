<!--
    @component
    Bold hero banner with eye-catching text and strong call-to-action. NEVER use title case.

    Usage:
    ```html
    <Hero
      title="Bold Claim"
      subtitle="Quick Value"
      imageSrc="https://www.unc.mn/image-placeholder.svg"
      callsToAction={[
        {
          href: "/start",
          label: "Go"
        },
        {
          href: "/learn",
          label: "More"
        }
      ]}
    />
    ```

    Props:
    - `title`: Main headline (string)
    - `subtitle`: Supporting text (string)
    - `imageSrc`: Hero image URL (string)
    - `callsToAction`: CTA buttons array (max two: primary, secondary)
-->

<script lang="ts">
	// Components
	import AnimateText from "$lib/components/animation/AnimateText.svelte";
	import Button from "$lib/components/ui/Button.svelte";

	// Constants
	import { cta } from "$lib/navigation";

	function handleImageError(e: Event) {
		const target = e.currentTarget as HTMLImageElement;
		target.src = "https://placehold.co/800x600/f8fafc/64748b?text=Hero+image";
	}

	// Types
	type Props = {
		centered?: boolean;
		title: string;
		subtitle: string;
		imageSrc?: string;
		callsToAction?: Array<{
			href: string;
			label: string;
		}>; // A maximum of two calls to action, with the first one being primary and the second one being secondary
		[key: string]: any;
	};

	let {
		title,
		subtitle,
		imageSrc,
		callsToAction = [cta],
		centered = false,
		...rest
	}: Props = $props();
</script>

<div class={[
	"bg-background relative overflow-hidden",
	"before:absolute before:inset-0 before:bg-gradient-to-br before:from-transparent before:via-transparent before:to-primary/5"
]} {...rest}>
	<header
		class={[
			"section-px container mx-auto grid items-end gap-16 gap-y-12 py-16 pt-32 text-balance relative z-10",
			centered ? "place-items-center text-center" : " xl:grid-cols-[1fr_auto]"
		]}
		data-enter-container
	>
		<div class="grid gap-8" class:max-w-prose={centered}>
			<div class="space-y-4">
				<h1 class="text-display w-full font-medium tracking-tight" data-enter>
					<span class="block text-foreground"><AnimateText text={title} /></span>
				</h1>
				{#if !centered}
					<p class="text-headline text-muted-foreground max-w-2xl leading-relaxed" data-enter>
						{subtitle}
					</p>
				{/if}
			</div>

			{#if centered}
				<p
					data-enter
					class={[
						"text-muted-foreground text-headline mx-auto block max-w-[45ch] transition duration-500 ease-out"
						// isTitleComplete ? "opacity-100" : "translate-y-2 opacity-0 blur-sm"
					]}
				>
					{subtitle}
				</p>
			{/if}
		</div>

		{#if callsToAction.length > 0}
			<div class="flex gap-4 pt-4" data-enter>
				{#each callsToAction as cta, index}
					<Button
						href={cta.href}
						size="lg"
						variant={index % 2 === 0 ? "primary" : "secondary"}
						class={[
							"max-lg:hidden transition-all duration-300",
							index % 2 === 0 ? "bg-primary hover:bg-primary/90 text-primary-foreground shadow-lg shadow-primary/20" : "border-border hover:bg-accent/50"
						]}>{cta.label}</Button
					>
					<Button
						href={cta.href}
						size="md"
						variant={index % 2 === 0 ? "primary" : "secondary"}
						class={[
							"lg:hidden transition-all duration-300",
							index % 2 === 0 ? "bg-primary hover:bg-primary/90 text-primary-foreground shadow-lg shadow-primary/20" : "border-border hover:bg-accent/50"
						]}>{cta.label}</Button
					>
				{/each}
			</div>
		{/if}
	</header>

	{#if imageSrc}
		<div class="col-span-full aspect-video relative z-10" data-enter>
			<div class="relative overflow-hidden rounded-lg border border-border/50">
				<img
					src={imageSrc}
					alt="Medical Affairs professionals achieving success"
					class="size-full object-cover transition-transform duration-500 hover:scale-105"
					onerror={handleImageError}
				/>
				<div class="absolute inset-0 bg-gradient-to-t from-background/20 via-transparent to-transparent"></div>
			</div>
		</div>
	{/if}
</div>
