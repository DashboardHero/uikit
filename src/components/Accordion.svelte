<script>
import { onMount } from 'svelte';

export let accordionElements;

onMount(() => {
        console.log("mounted");
		console.log(accordionElements);
	});

</script>

<ul uk-accordion style="color:white">
	{#each accordionElements as element}
    <li class=" { element.open == true ? "uk-open":"" } ">
        <a style="color:white" class="uk-accordion-title" href={element.href}> {element.title} </a>
        <div class="uk-accordion-content">
            <p> {element.content} </p>
        </div>
    </li>
    {/each}
</ul>
