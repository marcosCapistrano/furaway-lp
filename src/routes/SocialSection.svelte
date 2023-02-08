<script>
	import homem1 from '$lib/assets/comments/homem1.jpeg';
	import homem2 from '$lib/assets/comments/homem2.jpeg';
	import homem3 from '$lib/assets/comments/homem3.jpeg';
	import homem4 from '$lib/assets/comments/homem4.jpeg';
	import homem5 from '$lib/assets/comments/homem5.jpeg';

	import mulher1 from '$lib/assets/comments/mulher1.jpeg';
	import mulher2 from '$lib/assets/comments/mulher2.jpeg';
	import mulher3 from '$lib/assets/comments/mulher3.jpeg';
	import mulher4 from '$lib/assets/comments/mulher4.jpeg';
	import mulher5 from '$lib/assets/comments/mulher5.jpeg';

	const comments = [
		{
			author: 'Marilia Santos',
			timestamp: 'há 3 horas',
			content:
				'Achei esse trem maravilhooooso, funcionou super bem aqui e meu doguinho, que ama ser coçado kkkkkkk, amou ser penteado por ele, pega bem os pelo, dedicar uns 20min pela manhã e pela noite vai ser de grande ajuda a combater esse excesso de queda de pelo. Já fui no veterinário ver e ele disse que é normal, fiz exames nele e ele está super saudável, só é velhinho mesmo 🤗. Comprem sem medo de serem felizes 😅',
			image: mulher1
		},
		{
			author: 'Rafael Carvalho',
			timestamp: 'há 5 horas',
			content:
				'Produto conforme o especificado, muito satisfeito com o produto com o valor e com a entrega! pontas com acabamento em esfera protegendo além de bastante flexível.',
			image: homem1
		},
		{
			author: 'Maria Silva',
			timestamp: 'há 7 horas',
			content:
				'Tentei testar, mas meu gato tomou banho ontem, então não estava soltando muito pelo ainda kkk mas funciona e o melhor, ele não reclamou, então deve ser confortável pra ele. Produto conforme o anúncio e cumpre oq promete, vendedor enviou super rápido e enviou o rolinho de tirar pelos q pedi junto com cores combinando. Recomendo!',
			image: mulher2
		},
		{
			author: 'João Santos',
			timestamp: 'há 8 horas',
			content:
				'Hórus aprovou. 👍 Chegou bem rápido. É o ótimo, e esse botão atrás ajuda muito mesmo. Adoramos 😘',
			image: homem2
		},
		{
			author: 'Ana Paula',
			timestamp: 'há 10 horas',
			content:
				'O produto atendeu as especificações do vendedor. Muito fofinho, bonito e com o material muito bom. O vendedor postou rápido e chegou em Natal/RN em sete dias, muito rápido. Muito bem embalado.',
			image: mulher3
		},
		{
			author: 'Carlos Oliveira',
			timestamp: 'há 12 horas',
			content:
				'Amei a escova, pelo visto meu cachorro também kkkk ela é boa de pegar e as "cerdas" são flexíveis e não machucam. Muito mais fácil de tirar o excesso de pelos! A qualidade é ótima!',
			image: homem3
		},
		{
			author: 'Juliana Souza',
			timestamp: 'há 1 dia',
			content:
				'Amei! A qualidade é mt melhor do q eu achava q era, chegou certinho e bem embalado, o botão tira o pelo com facilidade (dá p apertar com 1 dedo só), a haste tem uma borracha q deixa mais confortável p segurar e as cerdas não machucam pq são abauladas. Eu tinha medo por ser ferro mas a escova não machucou minhas cachorras, ficaram super tranquilas enquanto as penteava. Desembaraçou todos os nós, mas não tirou alguns carrapichos pq as cerdas são mais separadas que os comuns. Mas funcionou perfeitamente e o pelo ficou mais macio e com menos frizz do que com a escova comum.',
			image: mulher4
		},
		{
			author: 'Paulo Almeida',
			timestamp: 'há 2 dias',
			content: 'Não poderia estar mais satisfeito com a minha compra',
			image: homem4
		},
		{
			author: 'Bruna Rodrigues',
			timestamp: 'há 3 dias',
			content: 'É simplesmente incrível, eu recomendo',
			image: mulher5
		},
		{
			author: 'Lucas Machado',
			timestamp: 'há 4 dias',
			content: 'O produto é ótimo e a entrega foi rápida, recomendo',
			image: homem5
		}
	];
</script>

<section class="social-proof">
	<div class="wrapper">
		<h1>O que dizem nossos clientes</h1>

		<span class="product__rating">
			<span class="rating__stars"><i>★</i><i>★</i><i>★</i><i>★</i><i>★</i></span>
			(857) avaliações
		</span>

		{#each comments as comment}
			<div class="comment row">
				<div class="profile-pic">
					<img src={comment.image} />
				</div>
				<div class="comment-content">
					<div class="header">
						<span class="author">{comment.author}</span>
						<span class="timestamp">{comment.timestamp}</span>
					</div>
					<div class="content">
						<p>{comment.content}</p>
					</div>
					<div class="footer">
						<div class="icon-btn">
							<i class="fa-solid fa-thumbs-up" />
							<span>Curtir</span>
						</div>

						<div class="icon-btn">
							<i class="fa-solid fa-reply" />
							<span>Responder</span>
						</div>
					</div>
				</div>
			</div>
		{/each}
	</div>
</section>

<style lang="scss">
	section.social-proof {
		background-color: #fff;
		color: #000;
		padding-top: 2rem;
		padding-bottom: 4rem;

		.product__rating {
			display: block;
			margin-top: 2rem;
			margin-bottom: 1rem;
			font-size: var(--step-2);
			.rating__stars {
				color: #fc0;
				text-shadow: #fc0 0 0 20px;
			}
		}

		.comment {
			margin: 1rem 0;
			border: 1px solid rgba(255, 255, 255, 0.25);
			padding: 1em;
			align-items: center;
			border-radius: 1em;

			.profile-pic {
				img {
					border-radius: 100%;
					max-width: 100%;
				}
			}

			.comment-content {
				width: 100%;
				margin-left: 1rem;
				line-height: 1.25;
			}
		}

		.icon-btn {
			cursor: pointer;
		}

		.header {
			display: inline-flex;
			align-items: baseline;
			gap: 10px;
			margin-bottom: 10px;

			.author {
				font-weight: bold;
			}

			.timestamp {
				font-size: 0.75em;
			}
		}

		.footer {
			display: inline-flex;
			gap: 16px;
			margin-top: 20px;
			.icon-btn {
				display: inline-flex;
				gap: 6px;
			}
		}
	}
</style>
