<script lang="ts">
	import Styles from '$lib/style/app.scss';
</script>

<body>
	<section class="AboutUs">
		<div class="Container">
			<div class="Tittle">ABOUT</div>
		</div>
		<div class="Container2">
			<div class="Opisy">
				<div class="Opis-First">
					Freelancer is a free bootstrap theme created by Start Bootstrap. The download includes the
					complete source files including HTML, CSS, and JavaScript as well as optional SASS
					stylesheets for easy customization.
				</div>
				<div class="Opis-Second">
					You can create your own custom avatar for the masthead, change the icon in the dividers,
					and add your email address to the contact form to make it fully functional!
				</div>
			</div>
		</div>
		<div class="Container3">
			<div class="Button">
				<button class="Download">Free Download!</button>
			</div>
		</div>
	</section>
	<slot />
</body>

<style lang="scss">
	.AboutUs {
		height: 70vh;
		width: 100%;
		background-color: #1abc9c;
		.Container {
			display: flex;
			justify-content: center;
			.Tittle {
				height: 10vh;
				width: 60%;
				display: flex;
				margin-top: 100px;
				justify-content: center;
				font-size: 64px;
				color: #ffffff;
				font-family: 'Montserrat', sans-serif;
			}
		}
		.Container2 {
			display: flex;
			justify-content: center;
			.Opisy {
				height: 30vh;
				width: 60vh;
				display: flex;
				justify-content: center;
				color: #ffffff;
				font-family: 'Montserrat', sans-serif;
				font-size: 22px;
			}
		}
		.Container3 {
			height: 10vh;
			width: 100%;
			display: flex;
			justify-content: center;
            .Download{
                height: 7vh;
                width: 23vh;
                font-size:22px;
                color: #ffffff;
                background-color: #1abc9c;
                border: solid 2px #ffffff;
                border-radius: 10px;
            }
            .Download:hover{
                    color: black;
                    background-color: #ffffff;
                    transition-duration: 2s;
            }
		}
	}
</style>
