<script>
	import logo from '$lib/assets/images/logo.svg';
	import openMenuIcon from '$lib/assets/images/icon-menu.svg';
	import closeMenuIcon from '$lib/assets/images/icon-menu-close.svg';
	import imgRetroPCs from '$lib/assets/images/image-retro-pcs.jpg';
	import imgTopLaptops from '$lib/assets/images/image-top-laptops.jpg';
	import imgGamingGrowth from '$lib/assets/images/image-gaming-growth.jpg';
	import imgWeb3Mobile from '$lib/assets/images/image-web-3-mobile.jpg';
	import imgWeb3Desktop from '$lib/assets/images/image-web-3-desktop.jpg';

	let menuOpen = $state(false);
</script>

<header>
	<img class="logo" src={logo} alt="Logo" />

	<button class="open onlg-hide" onclick={() => (menuOpen = !menuOpen)}>
		<img alt="Close Icon" src={menuOpen ? closeMenuIcon : openMenuIcon} class="menu-icon" />
	</button>

	<menu class={menuOpen ? '' : 'hide onlg-show'}>
		<nav>
			<ul>
				<li><a href="#home">Home</a></li>
				<li><a href="#new">New</a></li>
				<li><a href="#popular">Popular</a></li>
				<li><a href="#trending">Trending</a></li>
				<li><a onfocusout={() => (menuOpen = false)} href="#categories">Categories</a></li>
			</ul>
		</nav>
	</menu>
</header>

<main>
	<article class="article">
		<img class="article-image hide onlg-show" src={imgWeb3Desktop} alt="Web 3.0" />
		<img class="article-image onlg-hide" src={imgWeb3Mobile} alt="Web 3.0" />
		<h1 class="article-title">The Bright Future of Web 3.0?</h1>
		<p class="article-body">
			We dive into the next evolution of the web that claims to put the power of the platforms back
			into the hands of the people. But is it really fulfilling its promise?
		</p>
		<button class="article-cta">READ MORE</button>
	</article>
	<section class="featured-articles">
		<h2>New</h2>
		<article class="featured-article">
			<a href="#/hydrogen_vs_electric"
				><h3 class="featured-article-title">Hydrogen VS Electric Cars</h3></a
			>
			<p class="featured-article-body">Will hydrogen-fueled cars ever catch up to EVs?</p>
		</article>
		<article class="featured-article">
			<a href="#/downsides_of_ai"
				><h3 class="featured-article-title">The Downsides of AI Artistry</h3></a
			>
			<p class="featured-article-body">
				What are the possible adverse effects of on-demand AI image generation?
			</p>
		</article>
		<article class="featured-article">
			<a href="#/vc_funding"><h3 class="featured-article-title">Is VC Funding Drying Up?</h3></a>
			<p class="featured-article-body">
				Private funding by VC firms is down 50% YOY. We take a look at what that means.
			</p>
		</article>
	</section>

	<section class="articles-list">
		<article class="article-list-item">
			<img src={imgRetroPCs} alt="Retro PCs" />
			<h2>01</h2>
			<a href="#retro_pcs"><h3 class="article-list-item-title">Reviving Retro PCs</h3></a>
			<p class="article-list-item-body">What happens when old PCs are given modern upgrades?</p>
		</article>
		<article class="article-list-item">
			<img src={imgTopLaptops} alt="Top Laptops" />
			<h2>02</h2>
			<a href="#top_laptops"><h3 class="article-list-item-title">Top 10 Laptops of 2022</h3></a>
			<p class="article-list-item-body">Our best picks for various needs and budgets.</p>
		</article>
		<article class="article-list-item">
			<img src={imgGamingGrowth} alt="Gaming Growth" />
			<h2>03</h2>
			<a href="#gaming"><h3 class="article-list-item-title">The Growth of Gaming</h3></a>
			<p class="article-list-item-body">How the pandemic has sparked fresh opportunities.</p>
		</article>
	</section>
</main>
