<script lang="ts">
  import { onMount } from 'svelte';
  import Hero from '$lib/components/Hero.svelte';
  import TargetAudience from '$lib/components/TargetAudience.svelte';
  import CharacterShowcase from '$lib/components/CharacterShowcase.svelte';
  import Features from '$lib/components/Features.svelte';
  import HowItWorks from '$lib/components/HowItWorks.svelte';
  import Pricing from '$lib/components/Pricing.svelte';
  import CTA from '$lib/components/CTA.svelte';
  
  let mounted = false;
  
  onMount(() => {
    mounted = true;
  });
</script>

<svelte:head>
  <title>AI 인플루언서 플랫폼 - 나만의 AI 부캐로 팬들과 소통하세요</title>
  <meta name="description" content="버튜버, 유튜버, 인스타그램 인플루언서를 위한 AI 캐릭터 플랫폼. 팬들과 24/7 소통하고 새로운 수익을 창출하세요." />
</svelte:head>

<main class="min-h-screen bg-gradient-to-b from-gray-950 via-purple-950/20 to-gray-950">
  <Hero {mounted} />
  <TargetAudience />
  <CharacterShowcase />
  <Features />
  <HowItWorks />
  <Pricing />
  <CTA />
</main>