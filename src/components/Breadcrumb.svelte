<script>

export let breadcrumbItems = [
    {
        "href":"https://dashboardhero.dev",
        "item":"item1",
        "disabled":false,
        "active":false
    },
    {
        "href":"https://dashboardhero.dev",
        "item":"item2",
        "disabled":false,
        "active":false
    },
    {
        "href":"https://dashboardhero.dev",
        "item":"item3",
        "disabled":false,
        "active":false
    }
];

</script>

<ul class="uk-breadcrumb">
    {#each breadcrumbItems as breadcrumb}
        <li class={breadcrumb.disabled ? "uk-disabled":""}>
            <a href={breadcrumb.href}>{breadcrumb.item}</a>
        </li>
    {/each}
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
    <li class="uk-disabled"><a>Disabled</a></li>
    <li><span>Active</span></li>
</ul>