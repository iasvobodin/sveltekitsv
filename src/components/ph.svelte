<script>
	import photoseries from '../../static/db/Photoseries.json';
</script>

<h2 class="price__title">Фотосерии</h2>
<div class="photoseries">
	{#each photoseries as el}
		<a href="/photoseries/{el.Type}/{el.Route}">
			<img class="seriya" src={`/image/image2/1024_${el.PortraitFileName}.webp`} alt="" />
		</a>
	{/each}
</div>

<style>
	.photoseries {
		display: grid;
		grid-auto-flow: column;
		grid-auto-columns: 400px;
		height: calc(400px * 1.5);
		column-gap: 5px;
		max-width: 95%;
		margin: 0 auto;
		overflow-x: scroll;
		/* left: 50%; */
		position: relative;
		/* transform: translateX(-50%); */
	}
	.seriya {
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: center;
	}
</style>
