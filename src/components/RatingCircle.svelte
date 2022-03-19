<script>
  export let rating;
</script>

<div class="rating-circle">
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

  @media (hover: hover) and (pointer: fine) {
    .rating-circle:hover {
      background-color: var(--orange);
      color: var(--white);
    }
  }
</style>
