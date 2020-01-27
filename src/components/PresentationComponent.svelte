<script>

import DynamicGist from './DynamicGist.svelte';

export let componentName;
export let gistId;

</script>
<div class="uk-section uk-section-muted">
    <div class="uk-container">
<h1 style="color:#39f"> {componentName} </h1>
<div class="uk-child-width-expand@s" uk-grid style="background-color: #39f; padding-left: 20px; padding-top: 20px;padding-right:20px;">
    <div><slot id="component">  </slot></div>
    <div><DynamicGist gistId = {gistId} style="position:relative; height:300px"/></div>
</div>
    </div>
    </div>