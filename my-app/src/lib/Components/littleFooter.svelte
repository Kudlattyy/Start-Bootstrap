<body>
	<section class="Little-Footer">
		<div class="Component">
			<div class="Content">Copyright © Your Website 2023</div>
		</div>
	</section>

	<slot />
</body>

<style lang="scss">
	.Little-Footer {
		height: 10vh;
		width: 100%;
		background-color: var(--color-darkerblue);
		display: grid;
		place-items: center;
		.Component {
			height: 5vh;
			width: 100%;
			display: grid;
			place-items: center;
			.Content {
                font-size: var(--small-font-size);
                color: var(--base-font-color-white);
			}
		}
	}
</style>
