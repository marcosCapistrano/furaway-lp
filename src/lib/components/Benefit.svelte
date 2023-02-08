<script>
	// @ts-nocheck
	export let title;
	export let content;
	export let image;
	export let direction;
</script>

<div class="benefit-container">
	<div class="benefit-text {direction}">
		<div class="row">
			{#if direction === 'left'}
				<img src={image} alt="produto" class="col" />
				<div class="col left">
					<h2>{title}</h2>
					<p>
						{content}
					</p>
				</div>
			{:else}
				<div class="col right">
					<h2>{title}</h2>
					<p>
						{content}
					</p>
				</div>
				<img src={image} alt="produto" class="col" />
			{/if}
		</div>
	</div>
</div>

<style lang="scss">
	.benefit-container {
		margin-bottom: 4rem;
		margin: 0 auto 4rem auto;
		h2 {
			font-size: var(--step-4);
			height: 1.8em;
		}

		p {
			font-size: var(--step-3);
			line-height: 1.2;
			font-weight: 300;
		}

		img {
			margin-top: 1rem;
			margin-bottom: 1rem;
			max-width: 100%;
			border-radius: 100%;
		}

		.row {
			align-items: center;
			flex-wrap: wrap;
			text-align: center;
		}

		img.col {
			margin-inline: auto;
		}
	}

	@media only screen and (min-width: 600px) {
		.benefit-container {
			width: 100%;
		}

		.row {
			flex-wrap: nowrap;
			text-align: left;
		}

		.col {
			width: 45%;
		}

		.left {
			text-align: left;
			align-items: flex-start;
		}

		.right {
			text-align: right;
			align-items: flex-end;
		}

	}

	@media only screen and (min-width: 900px) {
		.benefit-container {
			h2 {
				font-size: var(--step-3);
			}

			p {
				font-size: var(--step-1);
			}
		}
	}
</style>
