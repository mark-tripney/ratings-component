<script>
  import { onMount } from "svelte";
  import RatingCircle from "./RatingCircle.svelte";
  let circles;

  onMount(() => {
    const ratingGroup = document.querySelector(".rating-group");
    circles = ratingGroup.querySelectorAll(".rating-circle");
  });

  const removeClass = (e) => {
    circles.forEach((circle) => {
      circle.classList.remove("selected");
    });
    e.detail.classList.toggle("selected");
  };
</script>

<div class="rating-group">
  <RatingCircle rating="1" on:circleClick={removeClass} />
  <RatingCircle rating="2" on:circleClick={removeClass} />
  <RatingCircle rating="3" on:circleClick={removeClass} />
  <RatingCircle rating="4" on:circleClick={removeClass} />
  <RatingCircle rating="5" on:circleClick={removeClass} />
</div>

<style>
  .rating-group {
    display: flex;
    justify-content: space-between;
    margin-bottom: 1.5rem;
  }
</style>
