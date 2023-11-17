<script lang="ts">
</script>

<body>
	<section class="Navbar">
		<div class="Container">
			START BOOTSTRAP
			<div class="Content-Menu">
				<ul>
					<li>
						<a href="">Portfolio</a>
					</li>
					<li>
						<a href="">About</a>
					</li>
					<li>
						<a href="">Contact</a>
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

	.Navbar {
		height: 10.5vh;
		width: 100%;
		display: flex;
		align-items: center;
		position: fixed;
		z-index: 10;
		background-color: var(--base-color-blue);
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
			font-family: var(--base-font-bold);
			font-size: var(--big-font-size);
		}
	}

</style>
