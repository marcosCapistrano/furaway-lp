<script>
	// @ts-nocheck

	import productPreto from '$lib/assets/preto.jpg';
	import productPretoCombo from '$lib/assets/preto_combo.jpg';
	import productRosa from '$lib/assets/rosa.jpg';
	import productRosaCombo from '$lib/assets/rosa_combo.jpg';
	import productAzul from '$lib/assets/azul.jpg';
	import productAzulCombo from '$lib/assets/azul_combo.jpg';
	import productCinza from '$lib/assets/cinza.jpg';
	import productCinzaCombo from '$lib/assets/cinza_combo.jpg';
	import productRoxo from '$lib/assets/roxo.jpg';
	import productRoxoCombo from '$lib/assets/roxo_combo.jpg';

	let innerWidth = 0;
	let innerHeight = 0;
	$: isSmallWindow = innerWidth < 600;

	let endDate = new Date('Feb 01, 2023 23:59').getTime();
	let now, timeleft, days, hours, minutes, seconds;

	setInterval(() => {
		now = new Date().getTime();
		timeleft = endDate - now;

		days = Math.floor(timeleft / (1000 * 60 * 60 * 24));
		hours = Math.floor((timeleft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
		minutes = Math.floor((timeleft % (1000 * 60 * 60)) / (1000 * 60));
		seconds = Math.floor((timeleft % (1000 * 60)) / 1000);

		console.log(days);
	}, 1000);

	//https://store-by-stores.mycartpanda.com/checkout/63255984:5&63255985:5&63255986:5&63255987:5&63255988:5&discount=PORTALG8

	let variants = [
		{
			name: 'Preto',
			image: productPreto,
			imageCombo: productPretoCombo,
			id: '63255984'
		},
		{
			name: 'Rosa',
			image: productRosa,
			imageCombo: productRosaCombo,
			id: '63255985'
		},
		{
			name: 'Azul',
			image: productAzul,
			imageCombo: productAzulCombo,
			id: '63255986'
		},
		{
			name: 'Cinza',
			image: productCinza,
			imageCombo: productCinzaCombo,
			id: '63255987'
		},
		{
			name: 'Roxo',
			image: productRoxo,
			imageCombo: productRoxoCombo,
			id: '63255988'
		}
	];

	let selectedVariant = '63255984';

	$: console.log(selectedVariant);
	$: console.log(typeof selectedVariant);

	$: findSelectedVariant = (id) => {
		for (let variant of variants) {
			if (variant.id === id) return variant;
		}
	};
</script>

<svelte:window bind:innerWidth bind:innerHeight />

<section id="offer">
	<div class="wrapper">
		<p>Preço Promocional por Tempo Limitado</p>
		<h1>+Frete Grátis</h1>
	</div>

	<div class="timer">
		<p class="timer-string">Promoção acaba em {days} dia(s), {hours}:{minutes}:{seconds}</p>
		<p class="timer-substring">(ou até acabar todas as unidades)</p>
	</div>

	<div class="products wrapper row">
		<div class="product">
			<div class="product__container">
				{#if isSmallWindow}
					<h2>Headache Cap Pro</h2>
					<span class="product__title">1 Unidade</span>
					<div class="product__image">
						<img
							src={findSelectedVariant(selectedVariant).image}
							alt="Imagem e link do produto com desconto"
						/>
					</div>
					<div class="product__details">
						<span class="product__subtitle"
							>De <span class="crossed">R$313.54</span> por R$184,99</span
						>
						<span class="product__subsubtitle">12x <span class="price">R$15,41</span></span>
						<span class="product__discount">Economia de <span class="text-featured">41%</span></span
						>

						<br />
						<br />
						<form class="form-variants">
							<label for="variants">Escolha uma Cor:</label>
							<select name="variants" id="variants" bind:value={selectedVariant}>
								{#each variants as variant}
									<option value={variant.id}>{variant.name}</option>
								{/each}
							</select>
						</form>
						<a
							class="btn"
							href={`https://store-by-stores.mycartpanda.com/checkout/${selectedVariant}:1&discount=PORTALG8-1&hide-selector=${selectedVariant}`}
							>Comprar Agora</a
						>
					</div>
				{:else}
					<h2>Headache Cap Pro</h2>
					<div class="product__image">
						<img
							src={findSelectedVariant(selectedVariant).image}
							alt="Imagem e link do produto com desconto"
						/>
					</div>
					<div class="product__details">
						<span class="product__title">1 Unidade</span>
						<span class="product__subtitle"
							>De <span class="crossed">R$313.54</span> por R$184,99</span
						>
						<span class="product__subsubtitle">12x <span class="price">R$15,41</span></span>
						<span class="product__discount">Economia de <span class="text-featured">41%</span></span
						>

						<br />
						<br />
						<form class="form-variants">
							<label for="variants">Escolha uma Cor:</label>
							<select name="variants" id="variants" bind:value={selectedVariant}>
								{#each variants as variant}
									<option value={variant.id}>{variant.name}</option>
								{/each}
							</select>
						</form>
						<a
							class="btn"
							href={`https://store-by-stores.mycartpanda.com/checkout/${selectedVariant}:1&discount=PORTALG8-1&hide-selector=${selectedVariant}`}
							>Comprar Agora</a
						>
					</div>
				{/if}
			</div>
		</div>
		<div class="product featured">
			<div class="product__container">
				{#if isSmallWindow}
					<h2>Headache Cap Pro</h2>
					<span class="product__title">2 Unidades</span>
					<div class="product__image">
						<img
							src={findSelectedVariant(selectedVariant).imageCombo}
							alt="Imagem e link do produto com desconto"
						/>
					</div>
					<div class="product__details">
						<span class="product__subtitle"
							>De <span class="crossed">R$627,08</span> por R$282,19</span
						>
						<span class="product__subsubtitle">12x <span class="price">R$23,51</span></span>
						<span class="product__discount">Economia de <span class="text-featured">55%</span></span
						>

						<br />
						<br />
						<form class="form-variants">
							<label for="variants">Escolha uma Cor:</label>
							<select name="variants" id="variants" bind:value={selectedVariant}>
								{#each variants as variant}
									<option value={variant.id}>{variant.name}</option>
								{/each}
							</select>
						</form>
						<a
							class="btn btn-featured"
							href={`https://store-by-stores.mycartpanda.com/checkout/${selectedVariant}:2&discount=PORTALG8&hide-selector=${selectedVariant}`}
							>Comprar Agora</a
						>
					</div>
				{:else}
					<h2>Headache Cap Pro</h2>
					<div class="product__image">
						<img
							src={findSelectedVariant(selectedVariant).imageCombo}
							alt="Imagem e link do produto com desconto"
						/>
					</div>
					<div class="product__details">
						<span class="product__title">2 Unidades</span>
						<span class="product__subtitle"
							>De <span class="crossed">R$627,08</span> por R$282,19</span
						>
						<span class="product__subsubtitle">12x <span class="price">R$23,51</span></span>
						<span class="product__discount">Economia de <span class="text-featured">55%</span></span
						>

						<br />
						<br />
						<form class="form-variants">
							<label for="variants">Escolha uma Cor:</label>
							<select name="variants" id="variants" bind:value={selectedVariant}>
								{#each variants as variant}
									<option value={variant.id}>{variant.name}</option>
								{/each}
							</select>
						</form>
						<a
							class="btn btn-featured"
							href={`https://store-by-stores.mycartpanda.com/checkout/${selectedVariant}:2&discount=PORTALG8&hide-selector=${selectedVariant}`}
							>Comprar Agora</a
						>
					</div>
				{/if}
			</div>
		</div>
	</div>
</section>

<style lang="scss">
	section#offer {
		text-align: center;
		padding: 2rem;

		.wrapper {
			h1 {
				font-size: var(--step-5);
			}
		}

		.timer {
			margin-top: 2rem;
			h2 {
				color: red;
			}
			p {
				font-size: 1.25rem;
				margin-top: 1em;
			}
			.timer-string {
				font-size: 1.5rem;
			}
			.timer-substring {
				font-size: 1rem;
			}
		}
	}

	.products {
		margin-top: 2rem;
		display: flex;
		flex-wrap: wrap;

		.product {
			margin-bottom: 4rem;

			h2 {
				margin-top: 0.75em;
				color: #000;
			}

			&.featured {
				.product__container {
					border: 3px solid darkblue;
					box-shadow: 4px 4px 4px rgba(0, 0, 100, 0.75);
					color: #000;
				}
			}

			.product__container {
				border: 1px solid black;
				border-radius: 2em;
				padding: 1em;
				display: flex;
				flex-wrap: wrap;
				justify-content: center;
				align-items: center;
				box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.2);
				background-color: #fff;
				color: #000;

				img {
					width: 100%;
				}

				.product__image {
					// flex-basis: 35%;
					max-width: 320px;
				}

				.product__title {
					margin: 0.75em;
					font-size: var(--step-4);
					font-weight: bold;
				}

				.product__details {
					display: flex;
					flex-direction: column;
					align-items: center;
					justify-content: space-between;
					margin-bottom: 2em;

					.product__discount {
						margin-top: 0.75em;
						padding: 1em 1.5em;
						background-color: rgba(0, 0, 0, 0.5);
						text-transform: uppercase;
						color: white;
						font-weight: bold;
						border-radius: 1em;
						display: block;

						.text-featured {
							color: orange;
						}
					}

					.product__subtitle {
						font-size: var(--step-2);
						margin-top: 0.75em;

						.crossed {
							color: gray;
							text-decoration: line-through;
						}
					}

					.product__subsubtitle {
						font-size: var(--step-2);
						margin-top: 0.75em;

						.price {
							color: $accentColor;
							font-size: var(--step-5);
						}
					}

					a {
						margin-top: 2rem;
						font-size: var(--step-2);
					}
				}
			}
		}
	}

	@media only screen and (min-width: 600px) {
		.products {
			.product {
				margin: 1rem auto;
			}
		}
	}

	@media only screen and (min-width: 900px) {
		.products {
			.product {
				width: 45%;
			}
		}
	}
</style>
