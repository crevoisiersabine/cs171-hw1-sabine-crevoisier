1 - In the gist example, the current chart is not useful because there are no labels and there are no axes so it is 
not possible to determine what data is being represented and what trend the data is showing.

2 - The first g is used to define svg as a G element that translates the origin to the top-left corner of the chart area. 
The second g element contains all of the bars composing the bar chart, each of which is defined as a g (the final nested 
g). The middle g contains all the rect elements and has bound each data point to a text element - however this text 
has not been appended yet and this is why it not to appear in the DOM; by doing groups.append(d3.selectAll("text")), the 
text elements appear and the data is bound to each respective text element (under parent node: final g). The last g only contains one rect element (and one text element bound to the data once this is appended).

3 - Placing the text prior to the rect only causes a layering difference and hence if the rect elements are not transparent 
they may obscure some of the labels depending on where the labels have been placed.
