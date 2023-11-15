<script>
	import Avatar from '$lib/Avatar.png';
</script>

<body>
	<section class="Title">
		<div class="Container">
			<div class="Header">
				<img src={Avatar} alt="Guy-Icon" />
			</div>
			<div class="Content">
				<div class="Caption">START BOOTSTRAP</div>
				<div class="SVG" />
				<div class="Description">Graphic Artist - Web Designer - Illustrator</div>
			</div>
		</div>
		<slot />
	</section>
</body>

<style lang="scss">
	.Title {
		height: 80vh;
		width: 100%;
		background-color: var(--base-color-green);
		display: grid;
		place-items: center;
		.Container {
			height: 40vh;
			width: 50vw;
			display: grid;
			place-items: center;
		}
		.Content {
			display: flex;
			flex-direction: column;
			.Caption{
				font-size: var(--tittle-font-size);
				color: var(--base-font-color-white);
				font-family: var(--base-font-bold);
			}
			.Description{
				font-size: var(--base-font-size);
				color: var(--base-font-color-white);
				font-family: var(--base-font-slim);
			}
		}
	}
</style>
