<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import Hero from "$lib/components/layout/hero-sections/Hero.svelte";
	
	// Icons for Features
	import IconGitPullRequest from "~icons/lucide/git-pull-request";
	import IconNetwork from "~icons/lucide/network";
	import IconShield from "~icons/lucide/shield";
	import IconUsers from "~icons/lucide/users";
	import IconPlugZap from "~icons/lucide/plug-zap";
	import IconBrainCircuit from "~icons/lucide/brain-circuit";
</script>

<Hero
	title="Launch excellence starts with coordination"
	subtitle="Align your team in weeks, not quarters. Transform scattered data into clear, reliable workflows with AI-native knowledge coordination that keeps scientists in control."
	imageSrc="/generated/image-a-medical-affairs-professional-is-in-a-m.webp"
	callsToAction={[
		{
			href: "/demo",
			label: "See demo"
		},
		{
			href: "/contact",
			label: "Get started"
		}
	]}
/>
<LogoScroller label="" generating />

<Summary
	title="What we do"
	text="Equator delivers AI-native knowledge coordination specifically built for life sciences teams. We transform fragmented scientific data across Veeva, Salesforce, and spreadsheets into governed workflows that reduce manual work by 80%. Medical Affairs directors at biotech companies use our platform to manage KOL relationships and scientific insights while maintaining full GxP compliance and audit trails."
/>

<Testimonials
	testimonials={[
		{
			name: "Dr. Elena Rodriguez",
			position: "Medical Affairs Director",
			company: "Meridian Therapeutics",
			quote:
				"Equator eliminated 6 hours of daily manual data entry across our team. Our KOL engagement tracking went from fragmented spreadsheets to real-time insights with full audit trails—exactly what we needed for our CNS program launch.",
			image: "/generated/image-a-confident-hispanic-woman-in-her-40s-dr.webp"
		},
		{
			name: "Marcus Chen",
			position: "Head of Medical Communications",
			company: "Vertex Biosystems",
			quote:
				"The governed knowledge branching system gave us confidence to let AI handle routine updates while keeping our scientists in control. We cut scientific literature review time by 75% without sacrificing compliance.",
			image: "/generated/image-a-confident-asian-man-in-his-30s-marcus-.webp"
		},
		{
			name: "Dr. Priya Sharma",
			position: "VP Medical Affairs",
			company: "Innovate Biopharma",
			quote:
				"Equator's unified semantic graph transformed our siloed Veeva and Salesforce data into actionable workflows. Our launch readiness improved from 18 months to 12 weeks—a game changer for competitive advantage.",
			image: "/generated/image-a-confident-indian-woman-in-her-40s-dr-p.webp"
		}
	]}
/>

<Features
	title="AI-native knowledge coordination"
	subtitle="Built from the ground up for human-AI collaboration in life sciences"
	features={[
		{
			title: "Governed AI collaboration",
			description: "Scientists stay in control with GitHub-style pull requests for AI-proposed knowledge updates, ensuring expertise guides every decision.",
			icon: IconGitPullRequest,
			iconClass: "text-accent-purple"
		},
		{
			title: "Unified knowledge graph",
			description: "Replace fragmented Veeva, Salesforce, and spreadsheet data with a single semantic source of truth that connects everything.",
			icon: IconNetwork,
			iconClass: "text-accent-aqua"
		},
		{
			title: "GxP-ready compliance",
			description: "21 CFR Part 11 compliant from Day Zero with complete audit trails, so you never compromise on regulatory requirements.",
			icon: IconShield,
			iconClass: "text-accent-blue"
		},
		{
			title: "KOL intelligence layer",
			description: "Real-time HCP profiles with influence metrics, publications, and network graphs that transform relationship management.",
			icon: IconUsers,
			iconClass: "text-accent-purple"
		},
		{
			title: "Zero-configuration integration",
			description: "Deploy in weeks, not quarters with seamless connections to existing Veeva and Salesforce systems - no rip and replace.",
			icon: IconPlugZap,
			iconClass: "text-accent-aqua"
		},
		{
			title: "Real-time insight capture",
			description: "Automated meeting prep and insight capture reduces manual documentation by 80% while maintaining scientific rigor.",
			icon: IconBrainCircuit,
			iconClass: "text-accent-blue"
		}
	]}
/>
<AboutTeaser />
<CallToAction
	title="Ready to transform your launch readiness?"
	subtitle="Join the AI-native revolution in Medical Affairs"
	description="Stop losing hours to manual data entry and fragmented workflows. See how Equator's governed AI coordination can reduce your team's busywork by 80% while maintaining full compliance—deploy in weeks, not quarters."
	imageSrc="/generated/image-a-professional-medical-affairs-director-.webp"
	callsToAction={[
		{
			href: "/demo",
			label: "See demo",
			variant: "primary"
		},
		{
			href: "/contact",
			label: "Get started",
			variant: "secondary"
		}
	]}
/>
