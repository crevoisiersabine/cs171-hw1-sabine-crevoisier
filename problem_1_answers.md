1. Colspan="3" causes the row to span the width of three columns in the table.

2. The th elements containing "Rank" have the following styles applied to them:

align = "center". This is an HTML attritube as it is specified within tags.
The above style ensures that the text is centered in the cell.

padding: 3px; This is a CSS styling included in the curly brackets {}.
The above tag defines a spacing between the cell border and the text.

Other styles are applied but are inherited/cascading from parent elements and those are not included.

The css equivalent of <align = "center"> is {text-align:center}

The HTML equivalent of {padding: 3px;} is <cellpadding = "3">

3. The DOM inspector allows you to highlight elements of interest as you hover over the html which is useful to determine 
what part of html corresponds to what piece on the webpage. The difference between the HTML source and the DOM is that the 
source will show the HTML prior to any javscript being executed, which might be something of interest; on the other hand 
the DOM shows the HTML at its current state.
