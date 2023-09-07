<script lang="ts">
	const reviews: { author: string; message: string }[] = [
		{
			author: 'Karl-Olof',
			message:
				'Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit libero modi tempore magnam sit perferendis veniam doloremque ea sequi ipsum impedit voluptatibus, inventore repudiandae vero, dicta nam laudantium quae distinctio.'
		},
		{
			author: 'Britt-Marie',
			message:
				'Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit libero modi tempore magnam sit perferendis veniam doloremque ea sequi ipsum impedit voluptatibus, inventore repudiandae vero, dicta nam laudantium quae distinctio.'
		},
		{
			author: 'Kärstin',
			message:
				'Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit libero modi tempore magnam sit perferendis veniam doloremque ea sequi ipsum impedit voluptatibus, inventore repudiandae vero, dicta nam laudantium quae distinctio.'
		}
	];

	const openingHours: { weekday: string; time: string }[] = [
		{
			weekday: 'Mån-Tors',
			time: '11:00 - 21:00'
		},
		{
			weekday: 'Fre',
			time: '11:00 - 02:00'
		},
		{
			weekday: 'Lör',
			time: '12:00 - 02:00'
		},
		{
			weekday: 'Sön',
			time: '12:00 - 21:00'
		}
	];
</script>

<div class="absolute top-0 w-full">
	<div class="container px-4 my-6">
		<img class="h-16" src="/logo.png" alt="" />
	</div>
</div>

<div
	class="border-b-8 border-puffin-primary bg-cover bg-center bg-black/40 bg-blend-darken"
	style="background-image: url('/hero.jpg');"
>
	<div class="container py-48 text-gray-100 flex flex-col gap-8">
		<div class="flex flex-col gap-4">
			<h1
				class="text-3xl md:text-5xl xl:text-6xl text-center md:text-left text-white font-heading uppercase font-bold"
			>
				Växjös nya pizzeria
			</h1>

			<p class="max-w-lg xl:max-w-xl text-center md:text-left">
				Tony välkomnar alla gamla och nya kunder att komma och prova våra nya indiska rätter. Vi har
				många nyheter på vår meny så tveka inte. Ännu en nyhet är att vi på fredag och lördag har
				nattöppet till 02.00 för nattsudd-arna. På nattpriset tillkommer 20 kr extra.
			</p>
		</div>

		<div class="w-full flex flex-col md:flex-row md:items-center gap-6">
			<button class="bg-puffin-primary py-4 px-6">Beställ online</button>
			<button class="">Vår meny</button>
		</div>
	</div>
</div>

<div>
	<div class="container flex flex-col-reverse md:grid grid-cols-2 gap-12 py-24">
		<div class="flex justify-end max-h-96">
			<img class="object-cover" src="/about.jpg" alt="" />
		</div>

		<div class="flex flex-col justify-center gap-4 text-center md:text-left">
			<h2 class="text-4xl text-puffin-primary font-heading uppercase font-bold">Om oss</h2>
			<p>
				Lorem ipsum, dolor sit amet consectetur adipisicing elit. Repellendus commodi voluptas earum
				delectus assumenda dignissimos nihil nemo sequi quaerat totam, accusantium similique illum
				ratione neque doloremque eaque officia reiciendis quidem.
			</p>
		</div>
	</div>

	<div class="flex flex-col items-center justify-center flex-grow gap-4 py-20">
		<div class="relative">
			<h2 class="text-4xl text-puffin-primary font-heading uppercase font-bold">Recensioner</h2>
		</div>

		<div class="md:grid grid-cols-3 text-md text-center container text-base" id="reviews">
			{#if reviews}
				{#each reviews as review}
					<div class="px-8 py-4 flex flex-col gap-4">
						<p>
							{@html review.message}
						</p>
						<span class="font-bold">{review.author}</span>
					</div>
				{/each}
			{/if}
		</div>
	</div>
</div>

<div class="relative bg-puffin-primary">
	<div class="container md:grid grid-cols-2 gap-16">
		<div>
			<div class="hidden md:block absolute left-0 w-1/2 h-full">
				<div
					class="w-full h-full bg-cover bg-center"
					style="background-image: url('/order.jpg');"
				/>
			</div>
		</div>
		<div class="flex flex-col gap-6 text-gray-100 py-24">
			<div>
				<h2 class="text-4xl font-heading uppercase font-bold">HAR DU BRÅTTOM?</h2>
				<p class="">Beställ online eller via telefon!</p>
			</div>

			<div class="flex flex-col-reverse md:flex-row gap-3 md:gap-4">
				<a href={'tel:0470-163 36'}>
					<button class="text-white border py-3 px-5 w-fit flex items-center gap-2">
						<svg width="18" height="18" viewBox="0 0 36 36">
							<path
								fill="currentColor"
								d="M27.73 35.44a4.72 4.72 0 0 1-1-.11a33.91 33.91 0 0 1-16.62-8.75a32.71 32.71 0 0 1-9-16.25a4.58 4.58 0 0 1 1.35-4.28l4-3.85A2 2 0 0 1 8 1.66a2 2 0 0 1 1.45.87l5 7.39a1.6 1.6 0 0 1-.11 1.9l-2.51 3A18.94 18.94 0 0 0 16 20.71a19.26 19.26 0 0 0 6.07 4.09l3.11-2.47a1.64 1.64 0 0 1 1.86-.12l7.55 4.88A2 2 0 0 1 35 30.2l-3.9 3.86a4.74 4.74 0 0 1-3.37 1.38ZM7.84 3.64l-4 3.85a2.54 2.54 0 0 0-.75 2.4a30.7 30.7 0 0 0 8.41 15.26a31.9 31.9 0 0 0 15.64 8.23a2.75 2.75 0 0 0 2.5-.74l3.9-3.86l-7.29-4.71l-3.34 2.66a1 1 0 0 1-.92.17a20.06 20.06 0 0 1-7.36-4.75a19.49 19.49 0 0 1-4.87-7.2A1 1 0 0 1 10 14l2.7-3.23Z"
							/>
							<path fill="none" d="M0 0h36v36H0z" />
						</svg>
						0470-163 36
					</button>
				</a>
				<a href="https://www.foodora.se/restaurant/ueu8/pizzahuset-spetsamossen">
					<button
						class="text-white bg-puffin-dark border border-puffin-dark py-3 px-5 w-fit flex items-center gap-2 hover:gap-3 duration-150"
					>
						Foodora
						<svg class="rotate-90" width="18" height="18" viewBox="0 0 36 36">
							<path
								fill="currentColor"
								d="M27.66 15.61L18 6l-9.66 9.61A1 1 0 1 0 9.75 17L17 9.81v19.13a1 1 0 1 0 2 0V9.81L26.25 17a1 1 0 0 0 1.41-1.42Z"
							/>
							<path fill="none" d="M0 0h36v36H0z" />
						</svg>
					</button>
				</a>
			</div>
		</div>
	</div>
</div>

<footer class="bg-puffin-dark text-white">
	<div class="container text-center lg:text-left py-24 grid lg:grid-cols-2 gap-10">
		<div>
			<h2 class="font-heading text-3xl mb-2">Kontakt</h2>
			<div class="grid lg:grid-cols-2 gap-2">
				<div class="flex flex-col">
					<h4>Adress:</h4>
					<a href="https://goo.gl/maps/ze2hmz3SUCBqZFkBA" class="underline hover:no-underline">
						Ringsbergsvägen 7, <br />
						352 33 Växjö
					</a>
				</div>

				<div class="flex flex-col">
					<h4>Telefon:</h4>
					<a href={'tel:0470-163 36'} class="underline hover:no-underline"> 0470-163 36 </a>
				</div>
			</div>
		</div>

		<div>
			{#if openingHours}
				<h2 class="font-heading text-3xl mb-2">Öppetider</h2>
				<div class="grid lg:grid-cols-4 gap-2">
					{#each openingHours as day}
						<div class="flex flex-col">
							<span>{day.weekday}</span>
							<span>{day.time}</span>
						</div>
					{/each}
				</div>
			{/if}
		</div>
	</div>

	<div class="container pb-8 text-center">
		Copyright 2023 © Seabird Digital UD. Alla rättigheter förbehållna.
	</div>
</footer>
