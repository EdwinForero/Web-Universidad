<template>
<div class="contenedorTotal">
	<header class="contenedorHeader">
		<img class="contenedorHeader__imgLogo" src="../images/Logo.png" alt="logo">
		<div class="contenedorHeader__banner">
			<div class="contenedorHeader__filtro">
				
				<nav class="contenedorHeader__navegacion">
					
					<router-link to="/">Inicio</router-link>
					<router-link to="/contacto">Contacto</router-link>
					<router-link to="/login">Login</router-link>
				</nav>
	
				<h1>Universidad de las Tecnologias TIC</h1>
			</div>

		</div>
	</header>

	<main class="contenedorMain">


		<h2 class="mainTitulo">Razones para aprender sobre tecnologia</h2>
		<section class="contenedorMain__superior">
			<div >
				<h3>Necesidad Mundial</h3>
				<p>Aliquam quis lorem vel odio maximus sagittis sit amet sit amet velit. Vivamus urna risus, rutrum non
					diam sit amet, rutrum feugiat magna. Ut quis nibh nec nisl luctus tristique. Interdum et malesuada
					fames ac ante ipsum primis in faucibus. Sed ut justo ac leo dignissim iaculis. Aliquam tincidunt
					ipsum non sapien volutpat, a fermentum felis pellentesque.</p>
				<img class="contenedorMain__img" src="../images/img-1.jpeg" alt="Computadoras">
			</div>
			<div>
				<h3>Oportunidades</h3>
				<p>Aliquam quis lorem vel odio maximus sagittis sit amet sit amet velit. Vivamus urna risus, rutrum non
					diam sit amet, rutrum feugiat magna. Ut quis nibh nec nisl luctus tristique. Interdum et malesuada
					fames ac ante ipsum primis in faucibus. Sed ut justo ac leo dignissim iaculis. Aliquam tincidunt
					ipsum non sapien volutpat, a fermentum felis pellentesque.</p>
				<img class="contenedorMain__img" src="../images/img-2.jpeg" alt="Jovenes">
			</div>
			<div>
				<h3>Desarrollo personal</h3>
				<p>Aliquam quis lorem vel odio maximus sagittis sit amet sit amet velit. Vivamus urna risus, rutrum non
					diam sit amet, rutrum feugiat magna. Ut quis nibh nec nisl luctus tristique. Interdum et malesuada
					fames ac ante ipsum primis in faucibus. Sed ut justo ac leo dignissim iaculis. Aliquam tincidunt
					ipsum non sapien volutpat, a fermentum felis pellentesque.</p>
				<img class="contenedorMain__img" src="../images/img-3.jpeg" alt="Desarrollo">
			</div>
		</section>

		<section class="contenedorMain__inferior">
		<h2 class="mainTitulo">Nuestros Cursos</h2>

		<div class="cursos">
			<h3 class="cursos__titulo">Python</h3>
			<p class="cursos__texto">Aliquam quis lorem vel odio maximus sagittis sit amet sit amet velit.
				Vivamus urna risus, rutrum non diam sit amet, rutrum feugiat magna. Ut quis nibh nec nisl luctus
				tristique. Interdum et malesuada fames ac ante ipsum primis in faucibus. Sed ut justo ac leo
				dignissim iaculis. Aliquam tincidunt ipsum non sapien volutpat, a fermentum felis pellentesque.
				Integer maximus, lectus non interdum iaculis, neque quam ultrices lacus, ut tempus sem turpis a
				lorem. Etiam posuere mauris eu turpis suscipit fermentum. Duis dictum sem ac malesuada lacinia.
				Suspendisse vulputate nec metus ac ullamcorper.</p>
				
			<img class="curso__img" src="../images/img-4.jpeg" alt="Joven programando">
		</div>
		<div class="cursos">
			<h3 class="cursos__titulo">Java</h3>
			<img class="curso__img" src="../images/img-5.jpeg" alt="Codificacion Java">
			<p>Aliquam quis lorem vel odio maximus sagittis sit amet sit amet velit. Vivamus urna risus, rutrum
				non diam sit amet, rutrum feugiat magna. Ut quis nibh nec nisl luctus tristique. Interdum et
				malesuada fames ac ante ipsum primis in faucibus. Sed ut justo ac leo dignissim iaculis. Aliquam
				tincidunt ipsum non sapien volutpat, a fermentum felis pellentesque. Integer maximus, lectus non
				interdum iaculis, neque quam ultrices lacus, ut tempus sem turpis a lorem. Etiam posuere mauris
				eu turpis suscipit fermentum. Duis dictum sem ac malesuada lacinia. Suspendisse vulputate nec
				metus ac ullamcorper.</p>
		</div>
		<div class="cursos">
			<h3 class="cursos__titulo">Diseño Web</h3>
			<p>Aliquam quis lorem vel odio maximus sagittis sit amet sit amet velit. Vivamus urna risus, rutrum
				non diam sit amet, rutrum feugiat magna. Ut quis nibh nec nisl luctus tristique. Interdum et
				malesuada fames ac ante ipsum primis in faucibus. Sed ut justo ac leo dignissim iaculis. Aliquam
				tincidunt ipsum non sapien volutpat, a fermentum felis pellentesque. Integer maximus, lectus non
				interdum iaculis, neque quam ultrices lacus, ut tempus sem turpis a lorem. Etiam posuere mauris
				eu turpis suscipit fermentum. Duis dictum sem ac malesuada lacinia. Suspendisse vulputate nec
				metus ac ullamcorper.</p>
			<img class="curso__img" src="../images/img-6.jpeg" alt="Esquema de ideas">
		</div>

		</section>
	</main>

	<footer>
		<!-- <img src="images\Banner.png" alt="Pie de pagina"> -->
		<div class="contenedorFooter">
			<div class="contenedorFooter__banner">
				<nav class="navegacion-footer">
					<router-link to="/">Inicio</router-link>
					<router-link to="/contacto">Contacto</router-link>
					<router-link to="/login">Login</router-link>
				</nav>
			</div>
		</div>
	</footer>
</div>
</template>




<script>
// @ is an alias to /src


export default {
  name: 'Home',
  components: {
    
  }
}
</script>

<style scoped>
		.contenedorTotal {
			margin: 0 auto;
			padding: 0;
			font-size: 62.5%;
			/* esto se hace para que 1rem = 10px*/
			max-width: 1140px;
			font-size: 16px;
		}



		h1 {
			font-size: 3.0rem;
		}

		h2 {
			font-size: 2.4rem;
		}

		h3 {
			font-size: 1.8rem;
		}

		h4 {
			font-size: 1.2rem;
		}

		p {
			font-size: 1.1rem;
		}

		a {
			font-size: 1.8rem;
		}

		/** Header **/
		.contenedorHeader {
			
			background-image: url(../images/banner.jpeg);
			height: 280px;
			background-size: cover;
			background-repeat: no-repeat;
			background-position: center center;
			display: grid;
			grid-template-columns: 280px 860px;
		}

		.contenedorHeader__imgLogo {
			height: 280px;
			width: 280px;
		}

		.contenedorHeader__banner {

			position: relative;
		}
		.contenedorHeader__filtro {
			position: absolute;
			background-color: rgba(0, 0, 0, 0.7);
			width: 100%;
			height: 100%;
		}
		.contenedorHeader__banner h1 {
			text-align: center;
			margin-top: 120px;
			color: white;
			
		}
		.contenedorHeader__navegacion {
			display: flex;
			gap: 2rem;
			justify-content: right;
			margin-top: 50px;
			margin-right: 50px;
			
			
		}
		.contenedorHeader__navegacion a {
			
			color: white;
			text-decoration: none;
		}

		/** Main **/

		.mainTitulo {
			width: max-content;
			margin: 30px auto;

		}

		.contenedorMain {
			max-width: 80%;
			margin: 0 auto;

		}

		.contenedorMain__superior {
			display: grid;
			grid-template-columns: 1fr 1fr 1fr;
			column-gap: 2rem;
		}

		.contenedorMain__superior h3 {
			text-align: center;
			margin: 20px 0;
		}

		.contenedorMain__superior p {
			margin: 30px 0;
		}

		.contenedorMain__superior img {
			width: 100%;
			margin: auto;
			height: 700px;
		}
		.contenedorMain__img {
			max-height: 280px;
		}
		.contenedorMain__inferior {
			width: 100%;
			margin: 0 auto;
		}
		.cursos {
			display: grid;
			grid-template-columns: 50% 50%;
			column-gap: 2rem;
			margin-top: 50px;
		}

		.cursos__titulo {
			grid-column: 1 / 3;
			text-align: center;
			background-color:#E5E0DC;
			margin-bottom: 20px;
			padding: 10px 0;
		}
		.curso__img {
			width:100%;
			height: 220px;
		}


		/** Footer **/
		.contenedorFooter {
			margin-top: 80px;
			background-image: url(../images/banner.jpeg);
			height: 100px;
			background-size: cover;
			background-repeat: no-repeat;
			background-position: center center;
			position: relative;

		}
		
		.contenedorFooter__banner {
			position: absolute;
			background-color: rgba(0, 0, 0, 0.7);
			width: 100%;
			height: 100%;
			display: flex;
			align-items: center;
			justify-content:right;
			
		}
		.navegacion-footer {
			display: flex;
			gap: 2rem;
			padding-right: 2rem;
		}
		.navegacion-footer a {
			
			color: white;
			text-decoration: none;
		}
</style>
