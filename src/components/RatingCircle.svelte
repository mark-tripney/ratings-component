<script>
  import { createEventDispatcher } from 'svelte';
  import { userRating } from '../stores';
  export let rating;

  let selected = false;
  const dispatch = createEventDispatcher();

  const handleClick = (e) => {
    userRating.update((score) => (score = e.currentTarget.innerText));
    dispatch('circleClick', e.currentTarget);
  };
</script>

<div class="rating-circle" class:selected on:click={handleClick}>
  <p>{rating}</p>
</div>

<style>
  .rating-circle {
    background-color: var(--darkBlue);
    width: 42px;
    height: 42px;
    border-radius: 50%;
    display: grid;
    place-items: center;
    color: var(--mediumGrey);
    cursor: pointer;
  }

  .rating-circle p {
    font-size: 0.875rem;
  }

  @media (min-width: 440px) {
    .rating-circle {
      width: 51px;
      height: 51px;
      font-size: 0.875rem;
    }
  }

  .rating-circle.selected,
  .rating-circle.selected:hover {
    background-color: var(--mediumGrey);
    color: var(--white);
  }

  @media (hover: hover) and (pointer: fine) {
    .rating-circle:hover {
      background-color: var(--orange);
      color: var(--white);
    }
  }

  @media (min-width: 440px) {
    .rating-circle p {
      font-size: 1rem;
    }
  }
</style>
