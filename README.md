UIKit you know and love, easier to use with components. Demo here: http://getuikit-elements.surge.sh/

###Quick example

Instead of writing this:
```
<ul uk-accordion>
    <li class="uk-open">
        <a class="uk-accordion-title" href="#">Item 1</a>
        <div class="uk-accordion-content">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        </div>
    </li>
    <li>
        <a class="uk-accordion-title" href="#">Item 2</a>
        <div class="uk-accordion-content">
            <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor reprehenderit.</p>
        </div>
    </li>
    <li>
        <a class="uk-accordion-title" href="#">Item 3</a>
        <div class="uk-accordion-content">
            <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat proident.</p>
        </div>
    </li>
</ul>
```
You write just this:
```
<script>
  import Accordion from "../src/components/Accordion.svelte";
  
  	let accordionProps = [
      ...
	  ];
  
</script>

<Accordion accordionElements = {accordionProps}/>
```

### Get started

To get started, clone this repository. App.svelte is the main entry point - delete everything between <main> tags and start building your web app.

### Run

```npm run dev```
This also builds the web app to /public.

### Deploy

You can use surge, firebase or any other 3rd party service to deploy. The files to be deployed can be found in /public.
For instance, you can navigate to /public and type surge to deploy.

