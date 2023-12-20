<script>
	import ServiceCard from '$lib/components/home/ServiceCard.svelte';
	import ContactButton from '$lib/components/home/ContactButton.svelte';

	let servicesOffered = [
		{
			icon: 'fa-solid fa-pen-nib',
			title: 'Design',
			description: 'Style your proyect with a "functionality first" aproach where we mix your ideas and our experience to create something ment for you'
		},
		{
			icon: 'fa-solid fa-code',
			title: 'Web Dev',
			description: 'No need to spend overwhelmingly long hours figuring out how to make your ideas comes to life. Let us do the hard work'
		},
		{
			icon: 'fa-solid fa-person-chalkboard',
			title: 'Consulting',
			description: 'We provide consulting services to help you put your proyect or business online'
		}
	];
	let contactLinks = [
		{link: "https://wa.link/5c8q0h", 
		icon: "fa-brands fa-whatsapp", 
		name: "WhatsApp"},
		{link: "mailto:robinsk8a@gmail.com", 
		icon: "fa-solid fa-envelope", 
		name: "G-Mail"},
		{link: "https://www.linkedin.com/in/robinson8a/?locale=en_US", icon: "fa-brands fa-linkedin-in", 
		name: "LinkedIn"}
	]
</script>

<!-- HERO -->
<div class="hero" id="home">
	<div class="hero-text">
		<div class="hero__name">
			<h2 class="my-name">Robinson Ochoa</h2>
			<h3 class="what-i-do">Designer, Marteter, Engeneer</h3>
		</div>
		<div class="hero__quote">
			<p class="quote-first-line">Imagination is the beginning of creation.</p>
			<p class="quote-second-line">
				You imagine what you desire, you will what you imagine, and at last, you create what you
				will.
			</p>
			<p class="quote-author">-George Bernard Shaw</p>
		</div>
	</div>
	<img class="hero-img" src="photos/cat01.jpg" alt="A cat using a sweater" />
	<h1 class="hero-tagline title">Create is fun</h1>
</div>

<!-- SERVICES SECTION -->
<section class="services" id="services">
	<div class="services-container">
		<div class="services-headline">
			<h3>Want your project to level up?</h3>
			<div class="services__img">
				<img src="MarioLvlUpIcon.svg" alt="pixelart Mario">
			</div>
		</div>
		<div class="services__paragraphs">
			<p>We can help you to make your ideas comes true in the web</p>
			<p>Let’s build together a site you can be proud of</p>
		</div>
		<div class="services__cards">
      {#each servicesOffered as { icon, title, description}}
			  <ServiceCard serviceIcon={icon} serviceTitle={title} serviceDescription={description} />
      {/each}
		</div>
		<div class="services__title">
			<img class="services-fill" src="zigzagFill.svg" alt="">
			<h1 class="services-title title">Services</h1>
		</div>
	</div>
</section>

<!-- PORTFOLIO SECTION -->
<section class="portfolio" id="portfolio">
	<div class="portfolio__imgs">
		<iframe title="website concepts" src="https://www.behance.net/embed/project/183033433?ilo0=1" height="316" width="404" allowfullscreen lazyload frameborder="0" allow="clipboard-write" refererPolicy="strict-origin-when-cross-origin"></iframe>
		<iframe title="IST social media" src="https://www.behance.net/embed/project/183033217?ilo0=1" height="316" width="404" allowfullscreen lazyload frameborder="0" allow="clipboard-write" refererPolicy="strict-origin-when-cross-origin"></iframe>
		<iframe title="COTECNOVA portfolio" src="https://www.behance.net/embed/project/147198465?ilo0=1" height="316" width="404" allowfullscreen lazyload frameborder="0" allow="clipboard-write" refererPolicy="strict-origin-when-cross-origin"></iframe>
		<iframe title="Multibrand story social media" src="https://www.behance.net/embed/project/147192217?ilo0=1" height="316" width="404" allowfullscreen lazyload frameborder="0" allow="clipboard-write" refererPolicy="strict-origin-when-cross-origin"></iframe>
		<iframe title="Gametastic website concept" src="https://www.behance.net/embed/project/147191759?ilo0=1" height="316" width="404" allowfullscreen lazyload frameborder="0" allow="clipboard-write" refererPolicy="strict-origin-when-cross-origin"></iframe>
		<iframe title="Presentation card desing" src="https://www.behance.net/embed/project/147190325?ilo0=1" height="316" width="404" allowfullscreen lazyload frameborder="0" allow="clipboard-write" refererPolicy="strict-origin-when-cross-origin"></iframe>
	</div>
	<div class="portfolio-title">
		<h1 class="portfolio__title title" >Portfolio</h1>
		<i class="fa-solid fa-object-group portfolio__icon"></i>
	</div>
</section>

<!-- ABOUT SECTION -->
<section class="about" id="about">
	<div class="about-container">
		<div class="about__photo">
			<i class="fa-solid fa-cat about__icon"></i>
			<img class="photo" src="photos/profile-pic.png" alt="" />
		</div>
		<p class="about__text">
			I am a passionate graphic designer and web developer dedicated to creating impactful digital experiences. My background in industrial engineering and technology in marketing, coupled with my experience in graphic design and programming, has equipped me with a solid foundation in web design, UX/UI, and front-end development. My focus is on crafting engaging and functional solutions that connect with users and drive meaningful outcomes. I have experience in social media management, WordPress, digital campaigns, and programming in Python, HTML, CSS, and JavaScript. My Behance portfolio and GitHub projects are testament to my ability to translate creative ideas into technical solutions. I am seeking opportunities to apply my skills and enthusiasm in a tech-savvy environment, where I can continue to grow and make a difference.
		</p>
		<div class="about-title">
			<div class="about__bit">A bit</div>
			<h1 class="about__title title">About me</h1>
		</div>

	</div>
</section>

<!-- CONTACT SECTION -->
<section class="contact" id="contact">
	<h2 class="contact-header">¡¿Whut?!</h2>
	<p>¿Were you expecting a form of something?</p>
	<p>¿Why not making this more personal?</p>
	<ul class="contact-links">
		{#each contactLinks as { link, icon, name}}
			<li><ContactButton linkRef={link} linkIcon={icon} linkName={name} /></li>
		{/each}
	</ul>
	<h1 class="contact-title title">Contact me</h1>
</section>

<style>

	/* ----------------------------	 hero ------------------------ */

	.hero {
		max-width: var(--max-width);
		padding: 4rem 2rem;
		margin: 0 auto;
		display: grid;
		grid-template-columns: 2fr 1fr;
		grid-template-rows: auto 1fr;
		justify-content: space-evenly;
		align-items: center;
		background-image: radial-gradient(closest-side, rgb(6, 45, 48), var(--dark01));
	}
	.hero-text {
		--hero-base-size: 1.6rem;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: start;
		gap: 3rem;
		grid-column: 1;
		grid-row: 1;
	}
	.hero__name {
		display: flex;
		flex-direction: column;
		align-items: end;
	}
	.my-name {
		font-size: calc(var(--hero-base-size) * 3.33);
	}
	.what-i-do {
		color: var(--extra);
		text-shadow: 0 0 0.2rem rgba(253, 136, 26, 0.63);
		font-size: calc(var(--hero-base-size) * 1.33);
		margin-top: -1rem;
	}
	.hero__quote {
		margin-left: 2rem;
		font-size: calc(var(--hero-base-size) * 1.08);
		width: calc(var(--hero-base-size) * 25);
		font-weight: 500;
	}
	.quote-first-line {
		font-size: calc(var(--hero-base-size) * 1.25);
		color: var(--light02);
		line-height: 3rem;
		position: relative;
	}
	.quote-first-line::before {
		content: '"';
		font-size: 2.6rem;
		position: absolute;
		top: -0.4rem;
		left: -1.2rem;
	}
	.quote-second-line {
		position: relative;
	}
	.quote-second-line::after {
		content: '"';
		color: var(--light02);
		font-size: 2.6rem;
		position: absolute;
		bottom: -0.5rem;
		right: 1.4rem;
	}
	.quote-author {
		font-size: var(--hero-base-size);
		margin-top: 1rem;
		text-align: end;
		color: var(--light02);
	}
	
	.hero-img {
		--catimg-size: clamp(20rem, 30vw, 28rem);
		width: var(--catimg-size);
		height: var(--catimg-size);
		grid-column: 2;
		grid-row: 1;
		justify-self: right;
		object-fit: cover;
		object-position: 0 13%;
		border-radius: 50%;
		box-shadow: -0.1rem 0.1rem 1.6rem 0.2rem #96d7e248;
	}
	.title {
		font-size: var(--home-title);
	}
	.hero-tagline {
    text-transform: uppercase;
		text-shadow: 0 0 0.4rem var(--light01);
		grid-row: 2;
		grid-column: 1/3;
		text-align: center;
		font-size: calc(var(--home-title)* 0.9);
	}
	
	@media (max-width: 1140px) {
		.hero-text {
		--hero-base-size: 1.2rem;
		}
	}
	@media (max-width: 900px) {
		.hero {
			display: flex;
			flex-direction: column;
			align-items: center;
			gap: 2rem;
		}
	}
	@media (max-width: 530px) {
		.hero {
			padding-top: 3rem;
		}
		.my-name {
			margin-bottom: 0.8rem;
		}
		.hero-text {
			--hero-base-size: 0.8rem;
		}
		.quote-first-line {
			line-height: 1.5rem;
		}
		.quote-first-line::before {
			content: '"';
			font-size: 1.6rem;
		}
		.quote-second-line::after {
			content: '"';
			font-size: 1.6rem;
			right: 0.6rem;
		}
		.hero-img {
			--catimg-size: 15rem
		}
	}
		



	/* ----------------------- SERVICES ------------------------- */

	.services {
		background-color: var(--dark02);
		padding: 4rem 2rem;
	}
	.services-container {
		max-width: var(--max-width);
		margin: auto;
		display: flex;
		flex-direction: column;
	}
	.services-headline {
		font-size: 4rem;
		font-weight: 400;
		color: var(--extra);
		display: flex;
		align-items: center;
		gap: 1.5rem;
	}
	
	.services__img {
		background-color: var(--neutro);
		width: 5rem;
		aspect-ratio: 1/1;
		border-radius: 1rem;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	@keyframes jump-mario {
		0%   {transform: translateY(0);}
		50%  {transform: translateY(-2rem);}
		100% {transform: translateY(0);}
	}
	.services__img img {
		padding: 0.2rem;
    --img-size: 4rem;
    width: var(--img-size);
    height: var(--img-size);
	}
	.services__img img:hover {
		animation-name: jump-mario;
		animation-duration: 0.3s;
	}
	

	.services__paragraphs {
		display: flex;
		flex-direction: column;
		align-items: center;
		font-size: 3rem;
		gap: 1rem;
		margin: 2rem 0;
	}

	

	.services__cards {
		display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 1;
		gap: 3rem;
    margin: 2rem 0;
	}
  .services__title {
    max-width: var(--max-width);
    display: flex;
    align-items: baseline;
    justify-content: space-between;
  }
  .services-fill {

    width: clamp(3rem, 34dvw, 38rem);
  }
  .services-title {
    color: var(--light02);
  }
	
	@media (max-width: 1300px) {
		.services-headline {
			font-size: 3rem;
		}
		.services__img {
			width: 4rem;
		}
		.services__img img {
			--img-size: 3.4rem
		}
		.services__paragraphs {
			font-size: 2rem;
		}
	}
	@media (max-width: 900px) {
		.services-headline {
			font-size: 2rem;
		}
		.services__img {
			width: 3.6rem;
		}
		.services__img img {
			--img-size: 2.9rem
		}
		.services__paragraphs {
			font-size: 1.6rem;
		}
	.services__cards {
		display: flex;
		margin-inline: auto;
		flex-direction: column;
		align-items: center;
		max-width: 80%;
		gap: 1rem;
	}
	}

	@media (max-width: 720px) {
		.services-headline {
			font-size: 1.6rem;
		}
		.services__paragraphs {
			font-size: 1.2rem;
		}
	}

	/* --------------------- PORTFOLIO -------------------------- */

	.portfolio {
		max-width: var(--max-width);
		margin: 2rem auto;
		padding: 4rem 2rem;

	}
	.portfolio__imgs {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		column-gap: 1.5rem;
		row-gap: 1rem;
		margin-bottom: 3rem;
	}
	.portfolio-title {
		display: flex;
		align-items: flex-start;
		justify-content: space-between;
	}
	.portfolio__icon  {
		font-size: 4rem;
		color: var(--dark01);
		background: var(--extra);
		padding: 1.5rem;
		border-radius: 50%;
		margin: auto;
	}
	@media (max-width: 720px) {
		.portfolio__icon  {
			font-size: 2rem;
			padding: 0.8rem;
		}
	}

	/* -------------------- ABOUT ------------------------ */

	.about {
		background-color: var(--dark02);
	}
	.about-container {
		max-width: var(--max-width);
		margin: 4rem auto;
		padding: 4rem 2rem;
		display: grid;
		grid-template-columns: 1fr 2fr;
		grid-template-rows: repeat(2, auto);
		align-items: center;
		justify-content: space-between;
		gap: 2rem ;
	}
	.about__photo {
		position: relative;
		grid-column: 1;
		grid-row: 1/3;
	}
	.about__icon {
		font-size: 2rem;
		position: absolute;
		top: 1rem;
		left: 1rem;
		padding: 1rem;
		background-color: var(--extra);
		color: var(--dark02);
		border-radius: 50%;
	}
	.photo {
		--about-photo-size: 22rem;
		width: var(--about-photo-size);
		height: var(--about-photo-size);
	}
	.about__text {
		font-size: 1.4rem;
		text-align: center;
		grid-column: 2;
		grid-row: 1;
	}
	.about-title {
		display: flex;
		align-items: center;
		justify-content: right;
		position: relative;
		grid-column: 2;
		grid-row: 2;
	}
	.about__title {
		color: var(--light01);
		font-size: calc(var(--home-title) * 0.9);
	}
	.about__bit {
		color: var(--dark02);
		font-size: 3rem;
		font-size: clamp(0.6rem, 2.4vw, 2.6rem);
		padding: 0 1.4rem;
		margin-left: -3rem;
		position: absolute;
		transform: rotate(90deg) translate(20%, 0%);
		left: 0;
		bottom: 50%;
		background-color: var(--light01);
	}

	@media (max-width: 1040px) {
		.about__photo {
			grid-column: 1;
			grid-row: 1;
		}
		.about-title {
			display: flex;
			transform: translate(10%, 0);
			justify-content: center;
			grid-column: 1/3;
			grid-row: 2;
		}
		.about__bit {
			left: 17%;
			padding-inline: 1rem;
		}
	}
	
	@media (max-width: 900px) {
		.about-container {
			display: flex;
			flex-direction: column;
			align-items: center;
		}
		.about-title {
			width: 100%;
			transform: translate(5%, 0);
		}
		.about__bit {
			padding-inline: 0.6rem;
		}
	}
	@media (max-width: 720px) {
		.about__text {
			font-size: 1.2rem;
		}
	}

	/* -------------------- CONTACT ---------------------------- */

	.contact {
		max-width: var(--max-width);
		margin: auto;
		padding: 4rem 2rem;
		font-size: 2.8rem;
		letter-spacing: 0.3rem;
		text-align: center;
		overflow-x: hidden;
	}
	.contact-header {
		text-align: center;
		font-size: 3rem;
		padding: 1.2rem;
		position: relative;
		isolation: isolate;
		margin-bottom: 2.5rem;
	}
	.contact-header::after {
		content: "";
		background-color: var(--neutro);
		position: absolute;
		inset: 0;
		z-index: -1;
		width: 100%;
	}
	.contact-links {
		margin-top: 4rem;
		margin-bottom: 2rem;
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 4rem;
	}
	@media (max-width: 1300px) {
		.contact {
			font-size: 2rem;
		}
	}
	@media (max-width: 1040px) {
		.contact-links {
			flex-direction: column;
		}
	}
	@media (max-width: 1300px) {
		.contact {
			font-size: 1.6rem;
		}
	}
	@media (max-width: 720px) {
		.contact-header::after {
			transform: translate(-10rem, 0);
		}
		.contact {
			font-size: 1.2rem;
	}
	@media (max-width: 530px) {
		.contact {
			letter-spacing: normal;
		}
	}

}


</style>
