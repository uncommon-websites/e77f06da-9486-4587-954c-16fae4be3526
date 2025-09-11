<!--
@component AboutTeaser
An engaging founder story teaser that builds personal connection and company credibility.
-->
<script lang="ts">
	// Types
	type TeamMember = {
		name: string;
		role: string;
		image: string;
	};

	// Components
	import Button from "../ui/Button.svelte";
	import ScrollText from "./sub/ScrollText.svelte";

	// State
	let sectionRef: HTMLElement;

	let props = $props();

	// Data - Authentic founder story for Equator
	const teamMember: TeamMember = {
		name: "Ragnar Öhman",
		role: "Founder & CEO",
		image: "/generated/image-a-professional-founder-headshot-featurin.webp"
	};

	// Compelling founder quote that reveals motivation and creates intrigue
	const founderQuote = "After watching brilliant scientists spend 40% of their time fighting fragmented data instead of advancing breakthrough therapies, I knew we had to build something different. The future of drug discovery isn't about replacing human expertise—it's about amplifying it with AI that actually understands how science works.";
</script>

<section bind:this={sectionRef} {...props} class="relative bg-card dark:bg-card">
	<div class="section-px section-py container mx-auto">
		<div class="relative mx-auto max-w-4xl">
			<!-- Founder Quote -->
			<div class="mb-12 text-center">
				<ScrollText
					class="text-title2 text-emphasis-high leading-relaxed"
					text={`"${founderQuote}"`}
				/>
			</div>

			<!-- Founder Details & CTA -->
			<div class="flex flex-col items-center gap-8 sm:flex-row sm:justify-center">
				<div class="flex items-center gap-4">
					<img
						src={teamMember.image}
						alt={teamMember.name}
						class="size-16 rounded-full object-cover border-2 border-accent-purple/20"
					/>
					<div class="text-center sm:text-left">
						<div class="text-callout font-medium text-emphasis-high">{teamMember.name}</div>
						<div class="text-caption text-emphasis-medium">{teamMember.role}</div>
					</div>
				</div>
				
				<Button 
					href="/about" 
					variant="secondary" 
					size="sm" 
					class="group relative overflow-hidden transition-all duration-300 hover:border-accent-purple/40"
				>
					<span class="relative z-10">Read the full story</span>
					<div class="absolute inset-0 bg-gradient-to-r from-accent-purple/0 via-accent-purple/5 to-accent-purple/0 opacity-0 transition-opacity duration-300 group-hover:opacity-100"></div>
				</Button>
			</div>

			<!-- Subtle background accent -->
			<div class="absolute -top-12 left-1/2 h-24 w-px bg-gradient-to-b from-accent-purple/20 via-accent-purple/10 to-transparent -translate-x-1/2"></div>
		</div>
	</div>
</section>
