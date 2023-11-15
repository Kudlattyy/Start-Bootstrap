<script lang="ts">
	import { fly } from 'svelte/transition';

	import Cabin from '$lib/Images/cabin.png';
	import Cake from '$lib/Images/cake.png';
	import Circus from '$lib/Images/circus.png';
	import Game from '$lib/Images/game.png';
	import Safe from '$lib/Images/safe.png';
	import Submarine from '$lib/Images/submarine.png';

	let boolean = false;

	function OpenMenu() {
		boolean = true;
	}

	function OffMenu() {
		boolean = false;
	}

	type oferta = {
		Tittle: string;
		src: string;
	};

	/*let oferty: oferta[] = [
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
	*/
</script>

<body>
	{#if boolean == true}
	<section class="Fly-Menu">
		<div class="Container" transition:fly={{ delay: 500, duration: 500 }}>
			<div class="Information-Menu">
				<button on:click={OffMenu}>Zamknij</button>
			</div>
		</div>
	</section>
	{/if}

	<section class="Portfolio">
		<div class="Containers">
			<div class="Header">Portfolio</div>
			<div class="Content">
				<div class="Projects">
					<div class="item item-1"><img class="Size" src={Cabin} alt="" on:click={OpenMenu} /></div>
					<div class="item item-2"><img class="Size" src={Cake} alt="" on:click={OpenMenu} /></div>
					<div class="item item-3">
						<img class="Size" src={Circus} alt="" on:click={OpenMenu} />
					</div>
					<div class="item item-4"><img class="Size" src={Game} alt="" on:click={OpenMenu} /></div>
					<div class="item item-5"><img class="Size" src={Safe} alt="" on:click={OpenMenu} /></div>
					<div class="item item-6">
						<img class="Size" src={Submarine} alt="" on:click={OpenMenu} />
					</div>
				</div>
			</div>
		</div>

		<slot />
	</section></body
>

<style lang="scss">
	@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@600&display=swap');
	.Portfolio {
		height: 100vh;
		width: 100%;
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
