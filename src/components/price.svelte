<script>
	import pricedata from '../../static/db/price.json';
</script>

<h2 class="price__title">Цены</h2>
<div class="price__image">
	<img
		src="https://raw.githubusercontent.com/iasvobodin/svs/images/static/image/webp/1024/19-03-02-20-58-27.webp"
		alt=""
	/>
</div>
<div class="price__holder">
	{#each pricedata as el}
		<div class="price__tarif">
			<h3>{el.title}</h3>
			<ul style="align-self: stretch;">
				{#each el.body as element}
					<li>{element}</li>
				{/each}
			</ul>
			<h4 style="align-self: end;justify-self: center;">
				Цена : {el.price}
			</h4>
		</div>
	{/each}
</div>

<style>
	.price__holder {
		display: grid;
		justify-content: center;
		grid-template-columns: repeat(auto-fill, minmax(max(25vw, 250px), 1fr));
		row-gap: 5vh;
		column-gap: 2vw;
		width: 90vw;
		margin: auto;
		color: white;
	}
	.price__image {
		width: 100%;
		height: 50vh;
		margin-bottom: 5vh;
	}
	.price__image > img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: 50% 40%;
	}
	.price__tarif {
		position: relative;
		display: grid;
		grid-template-rows: 10% min(30vh 600px) 10%;
		border-radius: 5px;
		padding: 3vh 1vw;
		background-image: repeating-linear-gradient(
				112.5deg,
				rgb(0, 0, 0) 0px,
				rgb(0, 0, 0) 14px,
				transparent 14px,
				transparent 15px
			),
			repeating-linear-gradient(
				22.5deg,
				rgb(0, 0, 0) 0px,
				rgb(0, 0, 0) 14px,
				transparent 14px,
				transparent 15px
			),
			linear-gradient(
				90deg,
				hsl(146, 54%, 44%),
				hsl(218, 54%, 44%),
				hsl(290, 54%, 44%),
				hsl(2, 54%, 44%),
				hsl(74, 54%, 44%)
			);
	}
	.price__tarif > h3 {
		align-self: start;
		justify-self: center;
		white-space: pre-wrap;
		text-align: center;
	}
	/* @counter-style repeating-emoji {
		system: cyclic;
		symbols: '🐏';
		suffix: ' ';
	} */

	/* // Add this class to the ul or ol element */
	.repeating-counter-rule {
		list-style-type: repeating-emoji;
	}
	.price__tarif > ul {
		align-self: stretch;
		margin-top: 5vh;
		margin-bottom: 5vh;
		/* list-style-type: '🐏 '; */
		/* list-style: none; */
		/* padding: 0;
		margin: 0; */
	}
	li {
		list-style-type: '🐏';
		padding-inline-start: 1ch;
	}
	/* .price__tarif > ul > li {
		padding-left: 1rem;
		text-indent: -0.7rem;
	} */

	/* .price__tarif > ul > li::before {
		content: '🐏  ';
	} */

	.price__tarif > h4 {
		place-self: center;
		white-space: pre-wrap;
	}
	/* .price__tarif::before {
    content: "";
    background: white;
    position: relative;
    width: calc(100% + 6px);
    height: calc(100% + 6px);
    z-index: 2;
  } */
	.price__title {
		font-family: Cormorant Infant;
		font-size: max(36px, 5.8vw);
		line-height: max(40px, 5.8vw);
		font-weight: 300;
		color: #ffffff;
		margin: 5vw;
	}
</style>
