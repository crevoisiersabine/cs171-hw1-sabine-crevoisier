1 - In the gist example, the current chart is not useful because there are no labels and there are no axes so it is 
not possible to determine what data is being represented and what trend the data is showing.

2 - The first g is used to define svg as a G element that translates the origin to the top-left corner of the chart area. 
The second g element contains all of the bars composing the bar chart, each of which is defined as a g (the final nested 
g). The middle g contains all the rect elements and all the text elements corresponding to the labels; the last g only 
contains one rect element.

3 - 
