<script>
  export let rating;
  let selected = false;

  const handleClick = (e) => {
    console.log(e.target.textContent);
    selected = !selected;
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
</style>
