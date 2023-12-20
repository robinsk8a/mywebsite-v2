<script>
  export let linkRef = "/"
  export let linkIcon = "fa-solid fa-carrot"
  export let linkName = "Name"
</script>

<a href={linkRef}>
  <i class={linkIcon}></i> 
  <span>
    {linkName}
  </span>
</a>

<style>
  a {
    background-color: var(--light01);
    font-size: 2rem;
    font-weight: 700;
    color: var(--dark01);
    padding: 1rem 0.5rem;
    border-radius: 60rem;
  }
  a i {
    background-color: var(--extra);
    padding: 1rem;
    border-radius: 50%;
  }
  a span {
    padding: 1rem;
  }
  @media (max-width: 530px) {
    a {
      font-size: 1.4rem;
      padding-block: 0.5rem;
    }
    a i {
      padding: 0.5rem;
    }
    a span {
      padding: 0.5rem;
    }
  }
</style>