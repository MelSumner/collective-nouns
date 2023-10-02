<script>
export let term = '';
export let definition = '';

definition = definition.replace(`${term}`, `<strong>${term.toLowerCase()}</strong>`);

</script>
<dt>{term}</dt>
<dd>{definition}</dd>
<style>/* Just leaving this here so it exists in the component */</style>