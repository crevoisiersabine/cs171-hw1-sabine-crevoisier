var color = d3.scale.linear()
  .domain([0, tbody.selectAll("tr")[0].length-1])
  .interpolate(d3.interpolateRgb)
  .range(["orangered", "silver"])
  
Question 1:
tbody.selectAll("tr") selects all the "tr" elements under the DOM element tbody. This is of type array of array and 
has length 1, ie. contains one element. In order to access that element (the array of "tr" elements) we must specify 
[0] and then apply.length to get the length of that array. Subtracting 1 just ensures that we do not overcount as we 
are starting from zero, instead of 1.

Question 2:
The function will return a string corresponding to a Rgb colour in between orangered and silver. Calling color(0) returns 
#ff4500; this should corresponds to orangered as the first value. color(150) returns #42ffff and color(10) returns #f25e26.
These colour strings are linear interpolations so that color(50) corresponds to silver and color(0) corresponds to orangered.
The reason it is a linear interpolation is specified by d3.scale.linear().

Question 3:
If the min and max values for rate were passed in domain, the linear interpolation would now occur from the min value of 
rate to the max value of rate. This would be appropriate if we wanted to visually encode different levels of unemployment 
and we could choose a colour scale where a low rate corresponded to a cold colour associated with a lower number and a warm 
colour might be associated with a higher value.
