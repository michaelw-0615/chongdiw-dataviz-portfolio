| [home page](https://cmustudent.github.io/tswd-portfolio-templates/) | [data viz examples](dataviz-examples) | [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

# Critique by Design: Meat Production in Germany, 2016-2023
In this project, I'll be redesigning the German meat production visualization published by the Statistisches Bundesamt (Federal Statistics Office of Germany) based on course contents and peer feedback.

## Step one: the visualization

The original data visualization of the German meat production issue was published in February on https://www.destatis.de/EN/Press/2023/02/PE23_051_413.html. 

<img src="Meat.jpg" width="1000"/>

## Step two: the critique
Upon first observation, a few things about this chart stood out to me: The three distinctly colored lines depicting pork, poultry and beef; the large title describing the subject “commercial meat production”, the timeline on the X-axis and the intersection of the three lines at year 2000 (which is weird after a second thought, since it’s highly unlikely that three categories of meat shares the same amount of production in a year). I think the chart works well in describing the subject, as well as displaying the overall tendencies of each category over time. However, I also find serious flaws in the design logics. First, the overall meat production, which is repeatedly mentioned in the associated article, is not reflected at all in the chart. Second, the Y-axis label does not stand for actual tonnages, but rather the ratio of each category compared to their respective amounts in 2000. This seriously weakens the intuitiveness and usefulness of the chart, since many viewers are expected to get more than just a tendency from the chart.

I expect that two groups will form the majority of my target audience: viewers of general news media and professional researchers. For the first group, the chart is largely effective, since the general public will only pay brief attention to the news report and will not dive into detailed figures. However, for the second group, this chart clearly fails to achieve the expected effectiveness. The counter-intuitiveness of the Y-axis labels, the absence of the total production tonnage as well as the vertically compressed lines (which hides the downwards tendency stated in the article) all make the chart hard to interpret quantitatively.

Therefore, I will focus most on improving the accuracy and intuitiveness of the chart, since this matters the most to the overall effectiveness. The example of simplifying the customer service performance chart on page 96-97 of the textbook serves as a good inspiration, since the simple line chart after modification that illustrates only the declining tendency is exactly what I want. To achieve better accuracy in data, I will definitely search for more data and solid evidence for meat production (especially figures after 2016) to include in my chart.

## Step three: Sketch a solution
Based on my critique above, I decided to a) cut the time range short to only 2016 and onwards; b) include actual tonnage figures rather than ratios. Hopefully, destatis.de has recorded detailed tonnage numbers for each category, so I naturally included them in my improved chart. To improve perceptiveness, I set the line for total tonnage red and others gray, since total production is what we want to talk about in the original article. Also, I changed the title to “Meat production in Germany shrinks for the 7th consecutive year” rather than just plain description in order to catch the eyes of viewers.

<div class='tableauPlaceholder' id='viz1758245833540' style='position: relative'>
  <noscript>
    <a href='#'>
      <img alt='Meat production in Germany shrinks for the 7th consecutive yearSource: https:&#47;&#47;www.destatis.de&#47; ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ge&#47;GermanMeatProductionDraft1&#47;1&#47;1_rss.png' style='border: none' />
    </a>
  </noscript>
  <object class='tableauViz'  style='display:none;'>
    <param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> 
    <param name='embed_code_version' value='3' /> 
    <param name='site_root' value='' />
    <param name='name' value='GermanMeatProductionDraft1&#47;1' />
    <param name='tabs' value='no' />
    <param name='toolbar' value='yes' />
    <param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ge&#47;GermanMeatProductionDraft1&#47;1&#47;1.png' /> 
    <param name='animate_transition' value='yes' />
    <param name='display_static_image' value='yes' />
    <param name='display_spinner' value='yes' />
    <param name='display_overlay' value='yes' />
    <param name='display_count' value='yes' />
    <param name='language' value='us-EN' />
    <param name='filter' value='publish=yes' />
  </object>
</div>         

<script type='text/javascript'>                    
  var divElement = document.getElementById('viz1758245833540');                    
  var vizElement = divElement.getElementsByTagName('object')[0];                    
  vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    
  var scriptElement = document.createElement('script');                    
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    
  vizElement.parentNode.insertBefore(scriptElement, vizElement);               
</script>

## Step four: Test the solution

I introduced the above solution to a few fellow students (whose personal information is hidden here) and asked about their impressions. The following are excerpts from their responses.


| Question | Interview 1 | Interview 2 | Interview 3 | Interview 4 |
|----------|-------------|-------------|-------------|-------------|
|What do you think works about this chart?|The detailed labels on the X and Y axes.|Lines that represent actual figures, not ratios.|             |             |
|What do you think didn't work well?|The lines look like competing groups rather than component categories.|             |The relations among the multiple lines are somewhat unclear.|Some lines have little to do with the total amount.|
|If you were to redesign, what might you try next?|             |Adding an average line of the total production amount over the years might help.|Adding a subtitle.|Perhaps we should not stick to the original line chart and try something new.|


## Step five: build the solution

Reflecting on the feedback from my peers, I feel that the original idea of depicting tonnage numbers in simple lines is still not engaging and intuitive enough. The lines for each category are separate from the total, which gives people a feeling that they’re not associated. Also, the gray color for breakdown categories make it hard for human eyes to catch in case some viewers do want a deeper dive into the figures. Therefore, a completely different design might be needed.

After that, I recalled the dataviz discussion before our first class and came up with the stack area chart, which was extremely similar to the mountains and snowlines of Wyoming that I previously posted. What about using the outlines of the Rocky Mountains to represent the total meat production tonnage, and dividing categories using the snowline?
<img src="Streamgraph.jpg" width="700"/>

By stacking sequential red-colored categories onto one another, we naturally get the outline of a decreasing total while still preserving independent categories which form parts of the total meat production. This way, the intuitiveness and perceptiveness get significantly improved, and the final solution looks indeed like a piece of meat (which is intentionally designed by me).

<div class='tableauPlaceholder' id='viz1758249242097' style='position: relative'>
  <noscript>
    <a href='#'>
      <img alt='Meat production in Germany shrinks for the 7th consecutive yearSource: https:&#47;&#47;www.destatis.de&#47; ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ge&#47;GermanMeatProductionDraft2&#47;1&#47;1_rss.png' style='border: none' />
    </a>
  </noscript>
  <object class='tableauViz'  style='display:none;'>
    <param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> 
    <param name='embed_code_version' value='3' /> 
    <param name='site_root' value='' />
    <param name='name' value='GermanMeatProductionDraft2&#47;1' />
    <param name='tabs' value='no' />
    <param name='toolbar' value='yes' />
    <param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Ge&#47;GermanMeatProductionDraft2&#47;1&#47;1.png' /> 
    <param name='animate_transition' value='yes' />
    <param name='display_static_image' value='yes' />
    <param name='display_spinner' value='yes' />
    <param name='display_overlay' value='yes' />
    <param name='display_count' value='yes' />
    <param name='language' value='en-US' />
    <param name='filter' value='publish=yes' />
  </object>
</div>                

<script type='text/javascript'>                    
  var divElement = document.getElementById('viz1758249242097');                    
  var vizElement = divElement.getElementsByTagName('object')[0];                    
  vizElement.style.width='100%';
  vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    
  var scriptElement = document.createElement('script');                    
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    
  vizElement.parentNode.insertBefore(scriptElement, vizElement);                
</script>

## References
All extra data used for creating the final design can be found by searching in the official Statistisches Bundesamt portal: https://www.destatis.de/EN/Home/_node.html.

## AI acknowledgements
ChatGPT 5 was used to help me navigate through Tableau. Other than that, all contents of this project are created with manual effort and without the involvement of GenAI.

