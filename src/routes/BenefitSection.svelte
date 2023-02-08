<script>
// @ts-nocheck

	import Carousel from 'svelte-carousel';
	import image1 from '$lib/assets/images/1.jpg';
	import image2 from '$lib/assets/images/2.jpg';
	import image3 from '$lib/assets/images/3.jpg';
	import image4 from '$lib/assets/images/4.jpg';
	import image5 from '$lib/assets/images/5.jpg';
	import image6 from '$lib/assets/images/6.jpg';

	let carousel;

	const handleNextClick = () => {
		carousel.goToNext();
	};
</script>

<section class="benefits">
	<div class="wrapper">
		<h1>Sobre o Produto</h1>
		<p>
			A FurAway foi pensada para aqueles donos que sofrem com a constante queda de pêlos de seu pet,
			querem cuidar de seu companheiro de uma forma simples e agradável para ele, e que não queiram
			ter de comprar outra escova tão cedo.
		</p>
		<p>
			A escova é construida com material plástico emborrachado e com cerdas de aço inoxidável.
			Garantindo que o produto seja reutilizável, durável e facilmente lavável, o processo de
			limpeza da escova é diferente das convencionais, onde o tutor precisa ficar retirando
			manualmente os pelos que foram capturados pela escova. Com a FurAway não, aperte o botão e
			todo o pêlo depositado é descartado em um instante! Use o tempo extra para se divertir com seu
			bixinho ou sua família!
		</p>

		<h2>Com ela você deixará de:</h2>
		<ul>
			<li>Passar horas escovando manualmente o pet, tendo mais tempo para se divertirem.</li>
			<li>
				Gastar dinheiro em escovas tradicionais que não são tão eficientes (e que por vezes machucam
				e estressam o animal)
			</li>
			<li>Se preocupar sempre que uma visita chega devido à sujeira espalhada</li>
			<li>Perder tempo retirando nós e emaranhados no pêlo do pet. Seu amiguinho agradecerá!</li>
			<li>Gastar dinheiro em serviços de tosa profissional.</li>
		</ul>

		<h2>E verá beneficios como:</h2>
		<ul>
			<li>
				Menos estresse e fadiga ao pet, que pode resultar em comportamentos mais calmos e felizes.
			</li>
			<li>
				Melhora na saúde do pet, já que a escovação regular ajuda a prevenir problemas de saúde
				relacionados ao pêlo, como nós e infecções.
			</li>
			<li>
				Melhor relacionamento entre o dono e o pet, já que a escovação regular é uma oportunidade
				para o dono fazer contato físico com o pet e fortalecer o vínculo.
			</li>
			<li>
				Menos necessidade de banhos frequentes para o pet, já que a escovação regular mantém o pêlo
				saudável e previne a acumulação de sujeira e cheiros indesejados.
			</li>
			<li>
				Maior autoestima e orgulho do dono em ter um pet bem cuidado, já que a escovação regular
				ajuda a manter o pet saudável e bonito.
			</li>
		</ul>

		<h1>Imagens</h1>
		<div class="carousel-container">
			<Carousel bind:this={carousel}>
				<img src={image1} alt="produto" class="carousel-img"/>
				<img src={image2} alt="produto" />
				<img src={image3} alt="produto" />
				<img src={image4} alt="produto" />
				<img src={image5} alt="produto" />
				<img src={image6} alt="produto" />
			</Carousel>
		</div>
		<!-- <div class="row"> -->
		<!-- </div> -->
	</div>
</section>

<style lang="scss">
	section.benefits {
		background-color: #fff;
		color: #000;
		padding: 2rem;

		.wrapper {
			text-align: left;
		}

		h1 {
			font-size: var(--step-5);
			margin-bottom: 1em;
			margin-top: 1em;
		}

		h2 {
			margin-top: 1.35em;
		}

		p {
			font-size: var(--step-1);
			text-align: left;
			line-height: 1.45;
		}

		ul {
			margin-top: 1rem;
			margin-bottom: 1rem;
			li {
				font-size: var(--step-1);
				line-height: 1.45;
			}

			li::before {
				content: '\B7';
				padding-right: 0.25em;
				font-size: var(--step-2);
				color: red;
			}
		}

		.carousel-container {
			max-width: 500px;
			margin: 0 auto;
		}
	}
</style>
