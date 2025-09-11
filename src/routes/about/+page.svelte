<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Governance is the foundation",
			description: "We believe trustworthy AI begins with oversight. Every AI-generated update in Equator is subject to governed review—modeled after software development's most rigorous standards. Like code reviews, each knowledge change is traceable, auditable, and controllable by your team. This is how we automate with confidence, without compromising compliance."
		},
		{
			title: "Science deserves structure",
			description: "Great science depends on clarity, continuity, and context. Our system turns fragmented sources into a single governed graph that retains domain-specific nuance while enabling AI-powered automation. By organizing knowledge the way scientists think, we reduce manual work—not rigor."
		},
		{
			title: "Keep humans in the loop",
			description: "We don't replace domain experts—we empower them. Equator's AI-native agents handle repetitive documentation and data harmonization while giving your team control over what changes. That means less time on spreadsheets, and more time on strategy, insight, and impact."
		}
	];
</script>

<SecondaryHero
	title="Mission control for launch excellence"
	subtitle="Built for GxP-compliant human-AI collaboration"
	imageSrc="/generated/image-a-diverse-team-of-data-scientists-and-li.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"Equator began with a simple frustration: brilliant scientific minds—especially in Medical Affairs—spending hours chasing down data, formatting spreadsheets, and reconciling inconsistencies between Veeva and Salesforce. These professionals didn't enter life sciences to become data entry clerks. They signed up to bring better therapies to patients. But with siloed systems and fragmented information, 40% of their time is lost to manual, repetitive tasks.",
		"We set out to change that. Equator is the first AI-native knowledge infrastructure built specifically for the nuance and rigor of life sciences—designed from the ground up to support GxP-compliant workflows while keeping scientists in full control. Unlike bolt-on AI wrappers, our platform uses a governed semantic graph, layered with explainable AI and human-in-the-loop collaboration. Think of it as GitHub for scientific knowledge coordination—every AI-generated update is traceable, auditable, and reversible.",
		"Today, Equator helps Medical Affairs teams unify insight collection, KOL engagement, and evidence planning across their entire ecosystem. Automating 80% of the busywork while maintaining full compliance isn't science fiction—it's already here. And we're just getting started. Our mission is to build the coordination layer that helps every team across life sciences move faster, safer, and more intelligently—so patients get the medicines they need, sooner."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- CTA Section -->
<CallToAction
	title="See knowledge coordination in action"
	subtitle="Book a demo"
	description="Ready to reduce manual work by 80% while maintaining GxP compliance? See how Medical Affairs teams use Equator to automate workflows across Veeva, Salesforce, and beyond—without replacing what already works."
	imageSrc="/generated/image-a-confident-medical-affairs-director-is-.webp"
/>
