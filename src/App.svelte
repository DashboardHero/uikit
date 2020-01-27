<script>
	// import the components
	import DynamicGist from "../src/components/DynamicGist.svelte";
	import Accordion from "../src/components/Accordion.svelte";
	import Alert from "../src/components/Alert.svelte";
	import Align from "../src/components/Align.svelte";
	import Article from "../src/components/Article.svelte";
	import Background from "../src/components/Background.svelte";
	import Badge from "../src/components/Badge.svelte";
	import PresentationComponent from "../src/components/PresentationComponent.svelte";
	
	// declare component properties as js objects - or retrieve from endpoint, db, etc
	let accordionProps = [
    {
        "href":"http://google.com",
        "title":"Accordion item 1",
        "content":"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.",
        "open":true
    },
    {
        "href":"http://facebook.com",
        "title":"Accordion item 2",
        "content":"Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        "open":false
    },
    {
        "href":"http://microsoft.com",
        "title":"Accordion item 3",
        "content":"Curabitur pretium tincidunt lacus. Nulla gravida orci a odio. Nullam varius, turpis et commodo pharetra, est eros bibendum elit, nec luctus magna felis sollicitudin mauris. Integer in mauris eu nibh euismod gravida. Duis ac tellus et risus vulputate vehicula. Donec lobortis risus a elit.",
        "open":false
	}
	];


	let articleProps = {
		"href":"http://microsoft.com",
		"heading": "Article heading",
		"author": "Jean Dena",
		"releaseDate": "01/25/2020",
		"content": "This is the article content"
	};
</script>

<main>
<!--
	Draw components on screen by specifying the component name
	Pass down props as propName = { inMemoryObject or object.functionCall() }
	<ComponentName propName = { propObject } />
-->
<a href="https://github.com/DashboardHero/uikit/blob/master/src/App.svelte"><Alert content= "See full source code for this page to see components in action"/></a>

<PresentationComponent componentName="Accordion" gistId="81bc43c63221008bc2c3c6b90d5540c6">
	<div><Accordion accordionElements = {accordionProps}/></div>
</PresentationComponent>


<PresentationComponent componentName="Alert" gistId="08ed2865818460fd42e5cee978658234">
	<div><Alert content = "Alert text"/></div>
</PresentationComponent>

<PresentationComponent componentName="Align" gistId="a2beb1cce00e973dd9ec9eef70ba2727">
	<div><Align/></div>
</PresentationComponent>


<PresentationComponent componentName="Article" gistId="4cc4d03b9ee9c6b6772e754e7f41211d">
	<Article  article = {articleProps}/>
</PresentationComponent>

<PresentationComponent componentName="Background" gistId="b9cfeed008760f5f6287b2bad85aaefe">
	<Background />
</PresentationComponent>

<PresentationComponent componentName="Badge" gistId="47ead78da6c56773e82567e1d2fdd5eb">
	<Badge text="Badge text"/>
</PresentationComponent>

</main>