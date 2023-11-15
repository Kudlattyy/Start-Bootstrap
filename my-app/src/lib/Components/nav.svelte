<body>
	<div class="Navbar">
		<div class="Container">
			START BOOTSTRAP
			<div class="Menu">
				<ul>
					<li>Portfolio</li>
					<li>About</li>
					<li>Contact</li>
				</ul>
			</div>
		</div>
	</div>
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
	}

	.Navbar {
		height: 11vh;
		width: 100%;
		background-color: #2c3e50;
		position: fixed;
		display: flex;
		align-items: center;
		z-index: 10;
		.Container {
			height: 9vh;
			width: 100%;
			display: flex;
			justify-content: space-between;
			margin-left: 10vw;
			align-items: center;
			color: #ffffff;
			font-family: 'Montserrat', sans-serif;
			font-size: 32px;
			.Menu {
				font-size: 24px;
				margin-right: 10vw;
			}
		}
	}
</style>
