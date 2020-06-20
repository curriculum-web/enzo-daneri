<script>
export let goals;
</script>



{#each goals as goal, index(goal.id)}s
 <h1>{name}</h1>
 <p>{description}</p>
{/each}