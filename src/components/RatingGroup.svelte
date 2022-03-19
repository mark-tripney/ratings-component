<script>
  import RatingCircle from "./RatingCircle.svelte";
</script>

<div class="rating-group">
  <RatingCircle rating="1" />
  <RatingCircle rating="2" />
  <RatingCircle rating="3" />
  <RatingCircle rating="4" />
  <RatingCircle rating="5" />
</div>

<style>
  .rating-group {
    display: flex;
    justify-content: space-between;
    margin-bottom: 1.5rem;
  }
</style>
