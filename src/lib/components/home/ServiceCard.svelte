<script>
  export let serviceIcon = "fa-solid fa-carrot"
  export let serviceTitle = "Title Gen"
  export let serviceDescription = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam tincidunt ante nibh, ut faucibus nulla tempor id."
</script>

<div class="card">
  <i class={serviceIcon} ></i>
  <div class="card__text-container">
    <h3 class="card__title">{serviceTitle}</h3>
    <p class="card__description">{serviceDescription}</p>
  </div>
</div>

<style>
  .card {
    padding: 2rem 3rem;
    background: rgb(46, 81, 87);
    color: var(--light01);
    border-radius: 1rem;
    position: relative;
    box-shadow: 0 0 0.6rem 0.1rem rgba(213, 244, 250, 0.3);
  }
  i {
    position: absolute;
    --position-ofset: -1rem;
    top: var(--position-ofset);
    left: var(--position-ofset);
    background-color: rgb(212, 167, 109);
    padding: 1rem;
    border-radius: 50%;
    font-size: 1.4rem;
    color: var(--dark02);
  }
  .card__title {
    font-size: 2rem;
    color: var(--light02);
    margin-bottom: 1rem;
    text-align: center;

  }
  .card__description {
    font-size: 1.2rem;
    font-weight: 500;
    text-align: center;
  }
  
</style>