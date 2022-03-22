<script>
  import { onMount } from 'svelte';
  import RatingCircle from './RatingCircle.svelte';
  let circles;
  let ratings = [1, 2, 3, 4, 5];

  onMount(() => {
    const ratingGroup = document.querySelector('.rating-group');
    circles = ratingGroup.querySelectorAll('.rating-circle');
  });

  const removeClass = (e) => {
    circles.forEach((circle) => {
      circle.classList.remove('selected');
    });
    e.detail.classList.toggle('selected');
  };
</script>

<div class="rating-group">
  {#each ratings as rating}
    <RatingCircle {rating} on:circleClick={removeClass} />
  {/each}
</div>

<style>
  .rating-group {
    display: flex;
    justify-content: space-between;
    margin-bottom: 1.5rem;
  }
  @media (min-width: 440px) {
    .rating-group {
      margin-bottom: 2rem;
    }
  }
</style>
