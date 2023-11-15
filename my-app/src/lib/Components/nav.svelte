<body>
	<section class="Navbar">
		<div class="Container">
			START BOOTSTRAP
			<div class="Content-Menu">
				<ul>
					<li>Portfolio</li>
					<li>About</li>
					<li>Contact</li>
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
	}

	.Navbar {
		height: 10vh;
		width: 100%;
		display: flex;
		align-items: center;
		position: fixed;
		z-index: 10;
		background-color: var(--base-color-blue);
		.Container {
			height: 10vh;
			width: 100%;
			display: flex;
			justify-content: space-between;
			align-items: center;
			margin-left: 10vw;
			color: var(--base-font-color-white);
			font-family: var(--base-font-bold);
			font-size: var(--big-font-size);
			.Content-Menu {
				margin-right: 10vw;
				font-family: var(--base-font-slim);
				font-size: var(--base-font-size);
			}
		}
	}
		@media screen and (max-width: 580px) {
 		 .navbar {
   		 padding: 20px 10px !important; 
  			}
		}
</style>
