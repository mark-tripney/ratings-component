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
    height: 360px;
    padding: 1.5rem;
  }

  :global(h1) {
    font-size: 1.5rem;
    color: var(--white);
    margin-bottom: 10px;
  }

  :global(.card-body-text) {
    font-size: 0.875rem;
  }

  @media (min-width: 440px) {
    .card {
      height: 416px;
      padding: 2rem;
    }
    :global(h1) {
      font-size: 1.75rem;
    }
    :global(.card-body-text) {
      font-size: 0.9375rem;
    }
  }
</style>
