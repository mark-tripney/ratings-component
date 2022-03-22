<script>
  export let buttonContent;
</script>

<button on:click>
  {buttonContent.toUpperCase()}
</button>

<style>
  button {
    background-color: var(--orange);
    color: var(--white);
    border: none;
    font-size: 0.875rem;
    letter-spacing: 2px;
    width: 100%;
    padding: 1em;
    border-radius: 22px;
    margin-bottom: 0.5rem;
    cursor: pointer;
  }

  @media (hover: hover) and (pointer: fine) {
    button:hover {
      background-color: var(--white);
      color: var(--orange);
    }
  }

  @media (min-width: 440px) {
    button {
      font-size: 0.9375rem;
    }
  }
</style>
