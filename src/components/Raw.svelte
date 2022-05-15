<script>
import raw from '../data/raw.json';
import refiner from '../data/refiner.json';
const getById = (id) => {
	return raw.find((p) => p.Id === id.Id);

};
</script>

<ul>
	{#each refiner as cat}
		<li>
			{#each cat.Inputs as input}
            {await getById(input)}
            {/each}
        </li>
	{/each}

    </ul>