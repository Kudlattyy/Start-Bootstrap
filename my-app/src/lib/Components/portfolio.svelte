<script lang="ts">
	import { fly } from 'svelte/transition';

	import Cabin from '$lib/Images/cabin.png';
	import Cake from '$lib/Images/cake.png';
	import Circus from '$lib/Images/circus.png';
	import Game from '$lib/Images/game.png';
	import Safe from '$lib/Images/safe.png';
	import Submarine from '$lib/Images/submarine.png';

	let boolean = false;
	let selectedImage = '';

	function OpenMenu(src: string) {
		boolean = true;
		selectedImage = src;
	}

	function OffMenu() {
		boolean = false;
		selectedImage = '';
	}

	type oferta = {
		Tittle: string;
		src: string;
	};

	let oferty: oferta[] = [
		{
			Tittle: 'Log Cabin',
			src: Cabin
		},
		{
			Tittle: 'Cake',
			src: Cake
		},
		{
			Tittle: 'Circus',
			src: Circus
		},
		{
			Tittle: 'Game',
			src: Game
		},
		{
			Tittle: 'Safe',
			src: Safe
		},
		{
			Tittle: 'Submarine',
			src: Submarine
		}
	];
</script>

<body>
	{#if boolean == true}
		<section class="Fly-Menu">
			<div class="Container" transition:fly={{ delay: 500, duration: 500 }}>
				<div class="Information-Menu">
					<button on:click={OffMenu}>Zamknij</button>
					{#if selectedImage}
						<img class="Size" src={selectedImage} alt="" />
					{/if}
				</div>
			</div>
		</section>
	{/if}

	<section class="Portfolio">
		<div class="Containers">
			<div class="Header">Portfolio</div>
			<div class="Content">
				<div class="Projects">
					{#each oferty as oferta}
						<div class="test">
							<img class="Size" src={oferta.src} alt="" on:click={() => OpenMenu(oferta.src)} />
						</div>
					{/each}
				</div>
			</div>
		</div>

		<slot />
	</section>
</body>

<style lang="scss">
	@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap');
	.Portfolio {
		height: 100vh;
		width: 100%;
		z-index: 100;
		.Header {
			height: 20vh;
			width: 100%;
			display: grid;
			place-items: center;
			font-family: var(--base-font-bold);
			font-size: var(--tittle-font-size);
			color: var(--base-font-color-blue);
		}
		.Content {
			height: 80vh;
			width: 100%;
			display: grid;
			place-items: center;
			.Projects {
				display: grid;
				grid-template-columns: 450px 450px 450px;
				grid-template-rows: 300px 300px;
				grid-gap: 50px;
				.Size {
					height: 300px;
					width: 450px;
					border-radius: 25px;
					transition-duration: 1s;
				}
				.Size:hover {
					filter: blur(5px);
				}
			}
		}
	}

	.Container {
		width: 100vw;
		height: 100%;
		display: grid;
		place-items: center;
		position: absolute;
		z-index: 10;
		overflow: hidden;
		background-color: rgba(37, 37, 37, 0.8);
		.Information-Menu {
			width: 50vw;
			height: 95vh;
			display: grid;
			place-items: center;
			border-radius: 10px;
			background-color: #ffffff;
		}
	}
</style>
