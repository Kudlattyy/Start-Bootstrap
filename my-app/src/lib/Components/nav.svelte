<script lang="ts">
	import { onMount } from 'svelte';

	let navbar;
	let container;
	let links;
	let currentPath;

	onMount(() => {
		window.addEventListener('scroll', () => {
			if (window.pageYOffset > 0) {
				navbar.style.height = '7vh';
				container.style.fontSize = 'calc(var(--big-font-size) * 0.8)';
				links.forEach((link) => (link.style.fontSize = 'calc(var(--smallest-font-size) * 0.8)'));
			} else {
				navbar.style.height = '10.5vh';
				container.style.fontSize = 'var(--big-font-size)';
				links.forEach((link) => (link.style.fontSize = 'var(--smallest-font-size)'));
			}
		});

		window.addEventListener(
			'hashchange',
			() => {
				currentPath = window.location.pathname;
			},
			false
		);

		currentPath = window.location.pathname;
	});

	function scrollIntoView(event) {
		event.preventDefault();
		const el = document.querySelector(event.currentTarget.getAttribute('href'));
		if (el) el.scrollIntoView({ behavior: 'smooth' });
	}
</script>

<body>
	<section class="Navbar" bind:this={navbar}>
		<div class="Container" bind:this={container}>
			START BOOTSTRAP
			<div class="Content-Menu">
				<ul>
					<li>
						<a
							bind:this={links}
							href=".Portfolio"
							on:click|preventDefault={scrollIntoView}
							class:active={currentPath === '.Portfolio'}>Portfolio</a
						>
					</li>
					<li>
						<a
							bind:this={links}
							href=".AboutUs"
							on:click|preventDefault={scrollIntoView}
							class:active={currentPath === '.AboutUs'}>About</a
						>
					</li>
					<li>
						<a
							bind:this={links}
							href=".contact"
							on:click|preventDefault={scrollIntoView}
							class:active={currentPath === '.contact'}>Contact</a
						>
					</li>
				</ul>
			</div>
		</div>
	</section>
	<slot />
</body>

<style lang="scss">
	@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap');

	ul {
		list-style: none;
	}

	li {
		display: inline-block;
		margin-right: 20px;
		margin-bottom: 1vh;
		text-transform: uppercase;
	}

	a {
		font-size: var(--smallest-font-size);
		color: var(--base-font-color-white);
		outline-color: transparent;
		text-decoration: none;
		transition: 0.3s;
	}

	a:hover {
		color: var(--base-color-green);
	}

	a.active {
		background-color: var(--base-color-green);
	}

	.Navbar {
		height: 10.5vh;
		width: 100%;
		display: flex;
		align-items: center;
		position: fixed;
		z-index: 10;
		background-color: var(--base-color-blue);
		transition: height 0.5s ease;
		.Container {
			height: 10vh;
			width: 82vw;
			padding-left: calc(var(--nav-padding-x) * 0.5);
			padding-right: calc(var(--nav-padding-x) * 0.8);
			display: flex;
			justify-content: space-between;
			align-items: center;
			margin-left: 10vw;
			color: var(--base-font-color-white);
			font-weight: 700;
			font-family: var(--base-font-bold);
			font-size: var(--big-font-size);
		}
	}
</style>
