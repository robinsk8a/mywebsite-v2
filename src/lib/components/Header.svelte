<header class="header">
  <div >
    <a class="branding" href="#home">
      <img class="logo" src="isologo2.svg" alt="" >
      <p>RobinSk8a</p>
    </a>
  </div>
  <nav class="nav">
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#portfolio">Portfolio</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>

<style>
  .header {
    padding: 0.5rem var(--sides);
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: var(--dark02);
    font-size: 1.2rem;
    font-weight: 500;
    width: 100%;
    position: sticky;
    top: 0;
    font-size: 1.4rem;
    z-index: 999;
  }

  /* BRANDING */
  .branding {
    display: flex;
    align-items: center;
    gap: 1rem;
  }
  .branding > * {
    cursor: pointer;
  }
  .branding p:hover {
    color: var(--light02);
    text-shadow: 0 0 0.4rem rgb(170, 218, 202);
  }
  .logo {
    --logo-max-size: 1.5rem;
    max-width: var(--logo-max-size);
    max-width: var(--logo-max-size);
  }

  /* NAV */
  .nav ul {
    display: flex;
    align-items: center;
    gap: 1rem;
  }
  .nav ul li:hover {
    color: var(--light02);
    text-shadow: 0 0 0.4rem rgb(170, 218, 202);
  }

  
  @media (max-width: 900px) {
    .header {
      font-size: 0.8rem;
    }
    .branding {
      gap: 0.4rem;
    }
    .logo {
      --logo-max-size: 1rem;
    }
  }
  @media (max-width: 530px) {
    .header {
      font-size: 1.4rem;
      font-weight: 700;
      letter-spacing: 0.2rem;
      justify-content: center;
    }
    .branding {
      gap: 1rem;
    }
    .logo {
      display: none;
    }
    .nav {
      display: none;
    }
  }
</style>