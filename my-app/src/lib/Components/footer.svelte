<body>
	<section class="Footer">
		<div class="Container">
			<div class="Titles">
				<ul class="Titles-Row">
					<li>LOCATION</li>
					<li>AROUND THE WEB</li>
					<li>ABOUT FREELANCER</li>
				</ul>
			</div>
			<div class="Descriptions">
				<ul class="Description-Row">
					<li>
						2215 John Daniel Drive<br />
						Clark, MO 65243
					</li>
					<li>svg here</li>
					<li>
						Freelance is a free to use,<br> MIT licensed Bootstrap theme created by <a
							href="https://startbootstrap.com/"
						/> .
					</li>
				</ul>
			</div>
		</div>
	</section>

	<slot />
</body>

<style lang="scss">
	.Footer {
		height: 40vh;
		width: 100%;
		background-color: var(--base-color-blue);
		display: grid;
		place-items: center;
		.Container {
			height: 10vh;
			width: 100vw;
			display: flex;
			justify-content: center;
			align-items: center;
            flex-direction: column;
		}
		.Titles-Row {
			width: 70vw;
			display: flex;
			justify-content: space-between;
			font-size: var(--big-font-size);
			font-family: var(--base-font-bold);
			color: var(--base-font-color-white);
		}
        .Description-Row{
            width: 75vw;
			display: flex;
			justify-content: space-between;
			font-size: var(--base-font-size);
			font-family: var(--base-font-slim);
			color: var(--base-font-color-white);
            text-align: center;
        }
	}

	ul {
		list-style: none;
	}
</style>
