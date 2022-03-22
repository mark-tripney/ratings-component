<div class="card">
  <slot />
</div>

<style>
  .card {
    border-radius: 15px;
    background-image: radial-gradient(
      circle at 50% 0%,
      #232a34 0%,
      #181e27 99%
    );
    width: 87%;
    max-width: 412px;
    padding: 1.5rem;
  }

  :global(h1) {
    font-size: 1.5rem;
    color: var(--white);
    margin-bottom: 10px;
  }
</style>
