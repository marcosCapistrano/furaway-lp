<footer>
	<div class="wrapper">
		<div class="details">
			<ul>
				<li>
					<span>© Copyright 2022-2023 StoreByStores</span>
				</li>
				<li>
					<span>CNPJ: 47.232.188/0001-67</span>
				</li>
				<li>
					<span>Contato: (35) 9 9846-1000</span>
				</li>
				<li>
					<span>Endereço: Travessia Evaristo da Veiga, 40, Centro, Pouso Alegre - MG</span>
				</li>
			</ul>
		</div>

		<div class="disclaimers">
			<ul>
				<li>
					<a href="https://www.storestores.com.br/pages/politicas-de-privacidade"
						>Políticas de Privacidade</a
					>
				</li>
				<li>
					<a href="https://www.storestores.com.br/pages/politicas-de-reembolso"
						>Política de Troca e Devolução</a
					>
				</li>
				<li>
					<a href="https://www.storestores.com.br/pages/politicas-de-frete">Políticas de Frete</a>
				</li>
				<li><a href="https://www.storestores.com.br/pages/aviso-legal">Termo de Uso</a></li>
			</ul>
		</div>
	</div>
</footer>

<style lang="scss">
	footer {
		background-color: 000;
		color: #fff;
		text-align: center;

		div.wrapper {
			display: flex;
			align-items: center;
			justify-content: space-between;
			padding-top: 1em;
			padding-bottom: 1em;

			li + li {
				margin-top: 1em;
			}

			.details {
				display: flex;
				flex-direction: column;
				text-align: left;
			}

			.disclaimers {
				display: flex;
				flex-direction: column;
				font-weight: bold;
				text-align: right;
				width: 100%;
			}
		}
	}

	// @media only screen and (min-width: 35rem) {
	// 	footer {
	// 		div.wrapper {
	// 			.disclaimers {
	// 				flex-direction: row;
	// 				justify-content: end;

	// 				a {
	// 					margin: 0.15em;
	// 				}
	// 			}
	// 		}
	// 	}
	// }
</style>
