<script>
	import Benefit from '$lib/components/Benefit.svelte';
	import natural from '$lib/assets/natural.jpg';
	import simples from '$lib/assets/simples.jpg';
	import gel from '$lib/assets/gel.jpg';
	import design from '$lib/assets/design.jpg';
	const benefits = [
		{
			title: 'A Origem',
			content:
				'Podemos passar o dia inteiro varrendo e aspirando a casa, mas 100% dos pêlos vem de seu pet, destes, 83% ou mais podem ser removidos apenas passando a escova uma vez ao dia.',
			// image: design,
			direction: 'left'
		},
		{
			title: 'A Escova',
			content:
				'A escova é construida com os materiais plástico, borracha, e aço inoxidável. Que pode ser simplesmente enxaguada após o uso. Sua função auto limpante faz com que até nos pets com maior incidência de queda de pelos a rotina seja fácil e rápida de ser aplicada',
			image: gel,
			direction: 'right'
		},
		{
			title: 'Não apenas estética',
			content:
				'A escovação não é importante apenas por questões estéticas. Além de promover maior hidratação das peles e pelos, seu animal deixará de sofrer de excesso de calor e desconfortos causados pelo excesso de pelos.',
			image: simples,
			direction: 'left'
		},
		{
			title: 'O Resultado',
			content:
				'Uma casa mais limpa com muito menos esforço. Uma amizade reforçada com o seu bixinho, com você e ele mais alegres e satisfeitos.',
			image: natural,
			direction: 'right'
		}
	];
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
			<li>Gastar dinheiro em escovas tradicionais que não são tão eficientes (e que por vezes machucam e estressam o animal)</li>
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
	}
</style>
