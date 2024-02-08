<script>
  // Importing the dictionary.json file
  import dictionary from './dictionary.json';

  // Accessing items from the imported dictionary
   // Accessing and sorting items alphabetically by term
   let sortedItems = dictionary.items.sort((a, b) => a.term.localeCompare(b.term));
</script>

<style>
  /* Your component styles here */
</style>

<dl>
  {#each sortedItems as item}
    <dt>{item.term}</dt>
    <dd>{item.definition}</dd>
  {/each}
</dl>


