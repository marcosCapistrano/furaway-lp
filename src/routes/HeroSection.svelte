<script>
	import heroVideo from '$lib/assets/heroVideo.mp4';
	import { onMount } from 'svelte';

	let innerWidth = 0;
	let innerHeight = 0;
	$: isSmallWindow = innerWidth < 900;
</script>

<svelte:window bind:innerWidth bind:innerHeight />

<section class="hero">
	<div class="wrapper">
		<div class="presentation row">
			<div class="hero-side">
				<video autoplay loop muted>
					<source src={heroVideo} />
				</video>
			</div>

			<div class="benefits-container">
				<h1>FurAway</h1>
				<p>
					Retome o controle da limpeza, garanta seu bem-estar e de quem mora com você. Cuide da
					saúde de seu pet de forma prática e fácil.
				</p>
				<ul class="benefits">
					<li>Acaba com mais de 83% do surgimento de pelos na casa.</li>
					<li>Diga adeus à ter de varrer a casa todos os dias.</li>
					<li>Restaure o brilho e felicidade de seu pet.</li>
					<li>Evite o desgaste entre tutor e pet, tenha mais tempo livre.</li>
					<li>Promove saúde de pele e pêlos do animal</li>
					<li>Não machuca!</li>
				</ul>

				<div class="other-benefits">
					<p>Outros benefícios:</p>

					<ul class="benefits">
						<li>Frete Grátis</li>
						<li>Promoção Limitada</li>
						<li>Garantia de 30 dias, direto do fornecedor</li>
					</ul>
				</div>
			</div>
		</div>
	</div>

	<div class="centered">
		<a href="#offer" class="btn btn-featured">Ver Ofertas</a>
	</div>
</section>

<style lang="scss">
	a.btn.btn-featured {
		margin: 0 auto;
		font-size: var(--step-2);
		padding: 1em 2.5em;
		margin-top: 2rem;
		display: inline-block;
		box-shadow: 0px 1px 4px rgba(255, 255, 255, 0.25);
	}
	.centered {
		text-align: center;
	}
	.row {
		display: block;
	}
	p {
		font-size: 1.2rem;
	}

	li {
		font-size: 0.8rem;
	}
	section.hero {
		margin-top: 3rem;
		margin-bottom: 4rem;
		text-align: center;

		img,
		video {
			max-width: 75%;
		}

		video {
			margin-top: 1rem;
			border-radius: 20%;
		}

		video.active {
			max-width: 50vw;
		}

		.leading {
			margin-top: 0.5em;
		}

		.heading {
			margin-top: 2em;
			font-weight: bold;
		}

		.presentation {
			p {
				margin-top: 0.5em;
				line-height: 1.2;
			}

			.benefits-container {
				margin-top: 4em;
				text-align: center;
				padding-inline: 1em;

				h1 {
					font-size: var(--step-5);
					margin-bottom: 2rem;
				}

				.benefits {
					margin-top: 2rem;
					line-height: 1.3;
					text-align: left;

					li::before {
						content: '\02713';
						padding-right: 0.5em;
					}
				}

				.other-benefits {
					margin-top: 2rem;
				}
			}
		}

		.hero-content {
			text-align: center;

			h1 {
				font-size: var(--step-5);
				color: darken($primaryColor, 5%);
				margin-bottom: 0.35em;
			}

			p {
				font-size: var(--step-1);
				color: darken($primaryColor, 50%);
				margin-bottom: 3em;
				line-height: 1.25;
			}

			.btn-container {
				text-align: center;
			}

			a {
				font-size: var(--step-1);
			}
		}
	}

	@media only screen and (min-width: 600px) {
		section.hero {
			text-align: left;
			video {
				max-width: 100%;
			}

			video.active {
				max-width: 80%;
			}
			.row {
				display: flex;
				align-items: center;
				justify-content: center;
			}
			.hero-side {
				width: 60%;
			}
			.benefits-container {
				width: 70%;
			}
			.hero-content {
				width: 80%;
			}
			.hero-image {
				width: 60%;
				align-self: flex-start;

				video {
					position: relative;
					width: 100%;
					max-height: 100%;
					min-width: 220px;
				}
			}

			.btn-container {
				width: fit-content;
			}
		}
	}
</style>
