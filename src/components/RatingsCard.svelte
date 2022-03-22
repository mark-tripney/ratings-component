<script>
  import Button from './Button.svelte';
  import Card from './Card.svelte';
  import RatingGroup from './RatingGroup.svelte';
  import { showThanks } from '../stores';

  const handleSubmit = () => {
    console.log('Clicked');
    showThanks.update((submitted) => (submitted = true));
  };
</script>

<Card>
  <div class="star-container">
    <svg
      class="svg-star"
      width="17"
      height="16"
      xmlns="http://www.w3.org/2000/svg"
      ><path
        d="m9.067.43 1.99 4.031c.112.228.33.386.58.422l4.45.647a.772.772 0 0 1 .427 1.316l-3.22 3.138a.773.773 0 0 0-.222.683l.76 4.431a.772.772 0 0 1-1.12.813l-3.98-2.092a.773.773 0 0 0-.718 0l-3.98 2.092a.772.772 0 0 1-1.119-.813l.76-4.431a.77.77 0 0 0-.222-.683L.233 6.846A.772.772 0 0 1 .661 5.53l4.449-.647a.772.772 0 0 0 .58-.422L7.68.43a.774.774 0 0 1 1.387 0Z"
        fill="#FC7614"
      /></svg
    >
  </div>
  <h1>How did we do?</h1>
  <p>
    Please let us know how we did with your support request. All feedback is
    appreciated to help us improve our offering!
  </p>
  <RatingGroup />
  <button on:click={handleSubmit}>Submit</button>
  <Button buttonContent="Submit" on:click={handleSubmit} />
</Card>

<style>
  .star-container {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background-color: var(--darkBlue);
    display: grid;
    place-items: center;
    margin-bottom: 1rem;
  }

  h1 {
    font-size: 1.5rem;
    color: var(--white);
    margin-bottom: 10px;
  }

  p {
    color: var(--lightGrey);
    margin-bottom: 2rem;
  }
</style>
