---
layout: page
title: Phrase Multiplier
permalink: /phrase-multiplier
comments: false
image: 
imageshadow: true
--- 


<!-- JavaScript Section -->
<script type="text/javascript">

function createResult()
{
	// for(phrases separated by \n ...)
	// separate into an array of substrings based on "\n"
	var itemsArray = document.getElementById("items").value.replace(/\r\n/g, "\n").split("\n");
	var numOfTimes = document.getElementById("number").value;
	var resultArray = [];
	// do some for loops to combine them all 
	for(i=0; i<itemsArray.length; i++) {
		for(j=0; j<numOfTimes; j++){
			resultArray.push(itemsArray[i]);
		}
	}

	writeResult(resultArray);
}

function writeResult(phraseArray)
{
	var resultTextArea = document.getElementById("result");
	resultTextArea.value = phraseArray.join("\n");
}

</script>

<!-- CSS Section -->



<div id="info">
		<p>Repeats a phrase a selected number of times.</p>
		<div class="leftColumn">
			<form>
				Number of Times: 
				<input id="number" type="text" value="4" />
					
			</form>	
		</div>	
	<div class="leftColumn">	
		<h4>Items List</h4>
		<textarea cols="50" id="items" placeholder="Enter items - one per line" rows="20"></textarea></div><div class="leftColumn"><br /></div><div class="leftColumn"><button id="resultsButton" onclick="createResult()" type="button">Do Stuff</button>
	</div>
	
	<div class="leftColumn">
	<h2 id="combinedH2"><br /></h2><h2 id="combinedH2">Result Phrases</h2>
		<textarea cols="50" id="result" rows="20"></textarea>
	</div></div>
