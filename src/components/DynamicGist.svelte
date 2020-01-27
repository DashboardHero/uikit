<script>
import { onMount } from 'svelte';

export let gistId;
let customId = Math.random();

onMount( () => {
    LoadGist(gistId);
});

function LoadGist(id) {
	if (id) {
		// Create an iframe, append it to this document where specified
		var gistFrame = document.createElement("iframe");
		gistFrame.setAttribute("width", "100%");
		gistFrame.setAttribute("height", "100%");
		gistFrame.id = "gistFrame"+customId;
	
		var zone = document.getElementById(customId);
		zone.innerHTML = "";
		zone.appendChild(gistFrame);
	
		// Create the iframe's document
		var gistFrameHTML = '<html><body onload="parent.adjustIframeSize(document.body.scrollHeight)"><scr' + 'ipt type="text/javascript" src="https://gist.github.com/' + id + '.js"></sc'+'ript><base target="_parent" /></body></html>';
	
		// Set iframe's document with a trigger for this document to adjust the height
		var gistFrameDoc = gistFrame.document;
	
		if (gistFrame.contentDocument) {
			gistFrameDoc = gistFrame.contentDocument;
		} else if (gistFrame.contentWindow) {
			gistFrameDoc = gistFrame.contentWindow.document;
		}
	
		gistFrameDoc.open();
		gistFrameDoc.writeln(gistFrameHTML);
		gistFrameDoc.close();
	}
}
	
function adjustIframeSize(newHeight) {
	var i = document.getElementById("gistFrame"+customId);
	i.style.height = parseInt(newHeight) + "px";
}


</script>

<div id={customId} scrolling="no" frameborder="0" style="position: relative; height:300px"></div>