<script>
export let term = '';
export let definition = '';
export let category = '';
definition = definition.replace(`${term.toLowerCase()}`, `<strong>${term.toLowerCase()}</strong>`);

</script>
<dt>{term}</dt>
<dd>
    <!-- since list-style-type none can mess with the default role attribute, redundantly declaring it as well -->
    <ul role="list">
        {#if category !== ''}
            <li class="category">Category: {category}</li>
        {/if}
        <li class="definition">{@html definition}</li>
    </ul>
</dd>
<style>
    ul {
        list-style-type: none;
        padding-left: 0;
        display: flex;
        flex-direction: column;
        gap: 0.25ch;
    }
    .category {
        font-size: 1.1rem;
    }
</style>