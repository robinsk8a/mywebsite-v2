<footer>
  <div class="footer">
    <div>
      <p>
        Designed and developed by Robinson Ochoa 2024
      </p>
      <small>
        © 2024 robinsk8a.com
      </small>
    </div>
    <div class="footer-links">
      <a href="https://github.com/robinsk8a">
        <i class="fa-brands fa-square-github"></i>
        <span>GitHub</span>
      </a>
      <a href="https://www.linkedin.com/in/robinson8a/?locale=en_US">
        <i class="fa-brands fa-linkedin"></i>
        <span>LinekIn</span>
      </a>
      <a href="https://www.behance.net/leronin8a8d7d">
        <i class="fa-brands fa-square-behance"></i>
        <span>Behance</span>
      </a>
    </div>
  </div>
</footer>

<style>
  footer {
    height: 10rem;
    background-color: var(--dark02);
  }
  .footer {
    padding: 2rem var(--sides);
    max-width: var(--max-width);
    margin-inline: auto;
    display: flex;
    justify-content: space-between;
    gap: 2rem;
  }
  .footer-links {
    display: flex;
    flex-direction: column;
    gap: 0.4rem;
    
  }
  .footer-links a:hover {
    color: var(--extra);
  }
  @media (max-width: 600px) {
    .footer-links {
      width: 100%;
    }
  }
  @media (max-width: 530px) {
    footer {
      font-size: 0.8rem;
    }
  }

</style>
