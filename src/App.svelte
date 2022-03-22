<script>
  import Footer from './components/Footer.svelte';
  import RatingsCard from './components/RatingsCard.svelte';
  import ThankyouCard from './components/ThankyouCard.svelte';
  import { showThanks } from './stores';
</script>

<main>
  {#if $showThanks}
    <ThankyouCard />
  {:else}
    <RatingsCard />
  {/if}
</main>
<Footer />

<style>
  main {
    flex: 1;
    display: grid;
    place-items: center;
  }
</style>
