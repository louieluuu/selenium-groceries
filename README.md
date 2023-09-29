# Auto Shopping List

Auto Shopping List is an automation script that web scrapes prices, stores them in a database, and e-mails sales to the user. Upon initialization, the database retains price history of the items you specify, and can be used to inform purchase decisions in a fashion similar to [camelcamelcamel](https://www.camelcamelcamel.ca/).

Built with Python, Selenium, and SQLite.

## Features

- **Modular**: supports multiple websites through OOP-like design
- **Multiprocessing**: scrapes multiple stores simultaneously

## Database Schema

<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" width="661px" viewBox="-0.5 -0.5 661 412" content="&lt;mxfile host=&quot;app.diagrams.net&quot; modified=&quot;2023-09-29T22:32:47.834Z&quot; agent=&quot;Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/117.0.0.0 Safari/537.36&quot; etag=&quot;Ac1ng4NfDRiw-V9b3htI&quot; version=&quot;22.0.0&quot;&gt;&#10;  &lt;diagram name=&quot;Page-1&quot; id=&quot;18Dh0pk9Mjt2kbTu2QYH&quot;&gt;&#10;    &lt;mxGraphModel dx=&quot;1195&quot; dy=&quot;632&quot; grid=&quot;1&quot; gridSize=&quot;10&quot; guides=&quot;1&quot; tooltips=&quot;1&quot; connect=&quot;1&quot; arrows=&quot;1&quot; fold=&quot;1&quot; page=&quot;1&quot; pageScale=&quot;1&quot; pageWidth=&quot;850&quot; pageHeight=&quot;1100&quot; math=&quot;0&quot; shadow=&quot;0&quot;&gt;&#10;      &lt;root&gt;&#10;        &lt;mxCell id=&quot;0&quot; /&gt;&#10;        &lt;mxCell id=&quot;1&quot; parent=&quot;0&quot; /&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-1&quot; value=&quot;Store&quot; style=&quot;rounded=0;whiteSpace=wrap;html=1;fontStyle=1;labelBackgroundColor=none;fillColor=#dae8fc;strokeColor=#6c8ebf;&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;120&quot; y=&quot;200&quot; width=&quot;120&quot; height=&quot;60&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-2&quot; value=&quot;Product&quot; style=&quot;rounded=0;whiteSpace=wrap;html=1;fontStyle=1;fillColor=#dae8fc;strokeColor=#6c8ebf;&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;480&quot; y=&quot;200&quot; width=&quot;120&quot; height=&quot;60&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-3&quot; value=&quot;Price History&quot; style=&quot;rounded=0;whiteSpace=wrap;html=1;fontStyle=1;fillColor=#dae8fc;strokeColor=#6c8ebf;&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;480&quot; y=&quot;430&quot; width=&quot;120&quot; height=&quot;60&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-4&quot; value=&quot;&quot; style=&quot;endArrow=none;html=1;rounded=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry width=&quot;50&quot; height=&quot;50&quot; relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;150&quot; y=&quot;200&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;131.76696810829094&quot; y=&quot;169.61161351381816&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-8&quot; value=&quot;&quot; style=&quot;endArrow=none;html=1;rounded=0;exitX=0.25;exitY=0;exitDx=0;exitDy=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot; target=&quot;0PQP1OqCxLKaKxkw8SD6-9&quot;&gt;&#10;          &lt;mxGeometry relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;510&quot; y=&quot;200&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;510&quot; y=&quot;200&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-9&quot; value=&quot;product url&quot; style=&quot;ellipse;whiteSpace=wrap;html=1;align=center;fontStyle=4;fillColor=#f8cecc;strokeColor=#b85450;&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;420&quot; y=&quot;140&quot; width=&quot;100&quot; height=&quot;40&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-29&quot; value=&quot;Owns&quot; style=&quot;shape=rhombus;perimeter=rhombusPerimeter;whiteSpace=wrap;html=1;align=center;fillColor=#d5e8d4;strokeColor=#82b366;&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;290&quot; y=&quot;200&quot; width=&quot;120&quot; height=&quot;60&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-36&quot; value=&quot;&quot; style=&quot;shape=link;html=1;rounded=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;424.90623372113237&quot; y=&quot;229.95311686056607&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;480&quot; y=&quot;229.91000000000003&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-37&quot; value=&quot;&quot; style=&quot;resizable=0;html=1;whiteSpace=wrap;align=right;verticalAlign=bottom;&quot; connectable=&quot;0&quot; vertex=&quot;1&quot; parent=&quot;0PQP1OqCxLKaKxkw8SD6-36&quot;&gt;&#10;          &lt;mxGeometry x=&quot;1&quot; relative=&quot;1&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-38&quot; value=&quot;product name&quot; style=&quot;ellipse;whiteSpace=wrap;html=1;align=center;fontStyle=0&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;525&quot; y=&quot;140&quot; width=&quot;100&quot; height=&quot;40&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-41&quot; value=&quot;cheapest price&quot; style=&quot;ellipse;whiteSpace=wrap;html=1;align=center;dashed=1;&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;640&quot; y=&quot;160&quot; width=&quot;100&quot; height=&quot;40&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-42&quot; value=&quot;avg price&quot; style=&quot;ellipse;whiteSpace=wrap;html=1;align=center;dashed=1;&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;640&quot; y=&quot;220&quot; width=&quot;100&quot; height=&quot;40&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-43&quot; value=&quot;avg sale price&quot; style=&quot;ellipse;whiteSpace=wrap;html=1;align=center;dashed=1;&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;640&quot; y=&quot;280&quot; width=&quot;100&quot; height=&quot;40&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-44&quot; value=&quot;&amp;lt;u&amp;gt;id&amp;lt;/u&amp;gt;&quot; style=&quot;ellipse;whiteSpace=wrap;html=1;align=center;fontStyle=0;fillColor=#f8cecc;strokeColor=#b85450;&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;360&quot; y=&quot;460&quot; width=&quot;100&quot; height=&quot;40&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-45&quot; value=&quot;store name&quot; style=&quot;ellipse;whiteSpace=wrap;html=1;align=center;fontStyle=4;fillColor=#f8cecc;strokeColor=#b85450;&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;80&quot; y=&quot;140&quot; width=&quot;100&quot; height=&quot;40&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-47&quot; value=&quot;price&quot; style=&quot;ellipse;whiteSpace=wrap;html=1;align=center;fontStyle=0&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;440&quot; y=&quot;510&quot; width=&quot;100&quot; height=&quot;40&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-48&quot; value=&quot;timestamp&quot; style=&quot;ellipse;whiteSpace=wrap;html=1;align=center;fontStyle=0&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;550&quot; y=&quot;510&quot; width=&quot;100&quot; height=&quot;40&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-49&quot; value=&quot;is_sale&quot; style=&quot;ellipse;whiteSpace=wrap;html=1;align=center;fontStyle=0&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;610&quot; y=&quot;460&quot; width=&quot;100&quot; height=&quot;40&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-50&quot; value=&quot;&quot; style=&quot;line;strokeWidth=1;rotatable=0;dashed=0;labelPosition=right;align=left;verticalAlign=middle;spacingTop=0;spacingLeft=6;points=[];portConstraint=eastwest;&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;240&quot; y=&quot;225&quot; width=&quot;50&quot; height=&quot;10&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-52&quot; value=&quot;&quot; style=&quot;shape=mxgraph.arrows2.wedgeArrow;html=1;bendable=0;startWidth=6.506024096385541;fillColor=strokeColor;defaultFillColor=invert;defaultGradientColor=invert;rounded=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry width=&quot;100&quot; height=&quot;100&quot; relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;435&quot; y=&quot;229.79999999999998&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;410&quot; y=&quot;229.9&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-54&quot; value=&quot;&quot; style=&quot;endArrow=none;html=1;rounded=0;exitX=0.25;exitY=0;exitDx=0;exitDy=0;entryX=0.415;entryY=0.975;entryDx=0;entryDy=0;entryPerimeter=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot; target=&quot;0PQP1OqCxLKaKxkw8SD6-38&quot;&gt;&#10;          &lt;mxGeometry relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;561&quot; y=&quot;200&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;540&quot; y=&quot;179&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-55&quot; value=&quot;Has&quot; style=&quot;shape=rhombus;perimeter=rhombusPerimeter;whiteSpace=wrap;html=1;align=center;fillColor=#d5e8d4;strokeColor=#82b366;&quot; vertex=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry x=&quot;480&quot; y=&quot;310&quot; width=&quot;120&quot; height=&quot;60&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-56&quot; value=&quot;&quot; style=&quot;endArrow=none;html=1;rounded=0;exitX=0.118;exitY=0.856;exitDx=0;exitDy=0;entryX=0.998;entryY=0.395;entryDx=0;entryDy=0;entryPerimeter=0;exitPerimeter=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot; source=&quot;0PQP1OqCxLKaKxkw8SD6-41&quot; target=&quot;0PQP1OqCxLKaKxkw8SD6-2&quot;&gt;&#10;          &lt;mxGeometry relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;571&quot; y=&quot;210&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;577&quot; y=&quot;189&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-57&quot; value=&quot;&quot; style=&quot;endArrow=none;html=1;rounded=0;entryX=1.015;entryY=0.356;entryDx=0;entryDy=0;entryPerimeter=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot; source=&quot;0PQP1OqCxLKaKxkw8SD6-42&quot;&gt;&#10;          &lt;mxGeometry relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;630&quot; y=&quot;235&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;600&quot; y=&quot;242&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-58&quot; value=&quot;&quot; style=&quot;endArrow=none;html=1;rounded=0;entryX=1;entryY=1;entryDx=0;entryDy=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot; source=&quot;0PQP1OqCxLKaKxkw8SD6-43&quot; target=&quot;0PQP1OqCxLKaKxkw8SD6-2&quot;&gt;&#10;          &lt;mxGeometry relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;625&quot; y=&quot;275&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;595&quot; y=&quot;282&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-59&quot; value=&quot;&quot; style=&quot;endArrow=none;html=1;rounded=0;exitX=0.949;exitY=0.286;exitDx=0;exitDy=0;exitPerimeter=0;entryX=-0.006;entryY=0.321;entryDx=0;entryDy=0;entryPerimeter=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot; source=&quot;0PQP1OqCxLKaKxkw8SD6-44&quot; target=&quot;0PQP1OqCxLKaKxkw8SD6-3&quot;&gt;&#10;          &lt;mxGeometry relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;425.00000000000017&quot; y=&quot;460.00000000000006&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;481.66&quot; y=&quot;445.8400000000001&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-60&quot; value=&quot;&quot; style=&quot;endArrow=none;html=1;rounded=0;exitX=0.641;exitY=0.003;exitDx=0;exitDy=0;exitPerimeter=0;entryX=0.25;entryY=1;entryDx=0;entryDy=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot; source=&quot;0PQP1OqCxLKaKxkw8SD6-47&quot; target=&quot;0PQP1OqCxLKaKxkw8SD6-3&quot;&gt;&#10;          &lt;mxGeometry relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;435.00000000000017&quot; y=&quot;470.00000000000006&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;489&quot; y=&quot;459&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-62&quot; value=&quot;&quot; style=&quot;endArrow=none;html=1;rounded=0;exitX=0.328;exitY=0.01;exitDx=0;exitDy=0;exitPerimeter=0;entryX=0.812;entryY=0.995;entryDx=0;entryDy=0;entryPerimeter=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot; source=&quot;0PQP1OqCxLKaKxkw8SD6-48&quot; target=&quot;0PQP1OqCxLKaKxkw8SD6-3&quot;&gt;&#10;          &lt;mxGeometry relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;560&quot; y=&quot;520&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;575&quot; y=&quot;498&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-63&quot; value=&quot;&quot; style=&quot;endArrow=none;html=1;rounded=0;exitX=0;exitY=0;exitDx=0;exitDy=0;entryX=1.012;entryY=0.409;entryDx=0;entryDy=0;entryPerimeter=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot; source=&quot;0PQP1OqCxLKaKxkw8SD6-49&quot; target=&quot;0PQP1OqCxLKaKxkw8SD6-3&quot;&gt;&#10;          &lt;mxGeometry relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;610&quot; y=&quot;471&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;625&quot; y=&quot;449&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-64&quot; value=&quot;&quot; style=&quot;shape=mxgraph.arrows2.wedgeArrow;html=1;bendable=0;startWidth=6.506024096385541;fillColor=strokeColor;defaultFillColor=invert;defaultGradientColor=invert;rounded=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry width=&quot;100&quot; height=&quot;100&quot; relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;540&quot; y=&quot;400.8&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;540&quot; y=&quot;371&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-71&quot; value=&quot;&quot; style=&quot;endArrow=none;html=1;rounded=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry width=&quot;50&quot; height=&quot;50&quot; relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;540&quot; y=&quot;310&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;540&quot; y=&quot;260&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-73&quot; value=&quot;&quot; style=&quot;shape=link;html=1;rounded=0;&quot; edge=&quot;1&quot; parent=&quot;1&quot;&gt;&#10;          &lt;mxGeometry relative=&quot;1&quot; as=&quot;geometry&quot;&gt;&#10;            &lt;mxPoint x=&quot;539.8062337211323&quot; y=&quot;390.0431168605661&quot; as=&quot;sourcePoint&quot; /&gt;&#10;            &lt;mxPoint x=&quot;539.81&quot; y=&quot;430&quot; as=&quot;targetPoint&quot; /&gt;&#10;          &lt;/mxGeometry&gt;&#10;        &lt;/mxCell&gt;&#10;        &lt;mxCell id=&quot;0PQP1OqCxLKaKxkw8SD6-74&quot; value=&quot;&quot; style=&quot;resizable=0;html=1;whiteSpace=wrap;align=right;verticalAlign=bottom;&quot; connectable=&quot;0&quot; vertex=&quot;1&quot; parent=&quot;0PQP1OqCxLKaKxkw8SD6-73&quot;&gt;&#10;          &lt;mxGeometry x=&quot;1&quot; relative=&quot;1&quot; as=&quot;geometry&quot; /&gt;&#10;        &lt;/mxCell&gt;&#10;      &lt;/root&gt;&#10;    &lt;/mxGraphModel&gt;&#10;  &lt;/diagram&gt;&#10;&lt;/mxfile&gt;&#10;" onclick="(function(svg){var src=window.event.target||window.event.srcElement;while (src!=null&amp;&amp;src.nodeName.toLowerCase()!='a'){src=src.parentNode;}if(src==null){if(svg.wnd!=null&amp;&amp;!svg.wnd.closed){svg.wnd.focus();}else{var r=function(evt){if(evt.data=='ready'&amp;&amp;evt.source==svg.wnd){svg.wnd.postMessage(decodeURIComponent(svg.getAttribute('content')),'*');window.removeEventListener('message',r);}};window.addEventListener('message',r);svg.wnd=window.open('https://viewer.diagrams.net/?client=1&amp;page=0&amp;edit=_blank');}}})(this);" style="cursor:pointer;max-width:100%;max-height:412px;"><defs/><g><rect x="40" y="60" width="120" height="60" fill="#dae8fc" stroke="#6c8ebf" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 118px; height: 1px; padding-top: 90px; margin-left: 41px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; font-weight: bold; white-space: normal; overflow-wrap: normal;">Store</div></div></div></foreignObject><text x="100" y="94" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle" font-weight="bold">Store</text></switch></g><rect x="400" y="60" width="120" height="60" fill="#dae8fc" stroke="#6c8ebf" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 118px; height: 1px; padding-top: 90px; margin-left: 401px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; font-weight: bold; white-space: normal; overflow-wrap: normal;">Product</div></div></div></foreignObject><text x="460" y="94" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle" font-weight="bold">Product</text></switch></g><rect x="400" y="290" width="120" height="60" fill="#dae8fc" stroke="#6c8ebf" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 118px; height: 1px; padding-top: 320px; margin-left: 401px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; font-weight: bold; white-space: normal; overflow-wrap: normal;">Price History</div></div></div></foreignObject><text x="460" y="324" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle" font-weight="bold">Price History</text></switch></g><path d="M 70 60 L 51.77 29.61" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 430 60 L 408.57 38.57" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="stroke"/><ellipse cx="390" cy="20" rx="50" ry="20" fill="#f8cecc" stroke="#b85450" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 98px; height: 1px; padding-top: 20px; margin-left: 341px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; text-decoration: underline; white-space: normal; overflow-wrap: normal;">product url</div></div></div></foreignObject><text x="390" y="24" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle" text-decoration="underline">product url</text></switch></g><path d="M 270 60 L 330 90 L 270 120 L 210 90 Z" fill="#d5e8d4" stroke="#82b366" stroke-miterlimit="10" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 118px; height: 1px; padding-top: 90px; margin-left: 211px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; white-space: normal; overflow-wrap: normal;">Owns</div></div></div></foreignObject><text x="270" y="94" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle">Owns</text></switch></g><path d="M 344.9 87.95 L 400 87.91 M 400 91.91 L 344.91 91.95 M 400 91.91" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="all"/><ellipse cx="495" cy="20" rx="50" ry="20" fill="rgb(255, 255, 255)" stroke="rgb(0, 0, 0)" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 98px; height: 1px; padding-top: 20px; margin-left: 446px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; white-space: normal; overflow-wrap: normal;">product name</div></div></div></foreignObject><text x="495" y="24" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle">product name</text></switch></g><ellipse cx="610" cy="40" rx="50" ry="20" fill="rgb(255, 255, 255)" stroke="rgb(0, 0, 0)" stroke-dasharray="3 3" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 98px; height: 1px; padding-top: 40px; margin-left: 561px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; white-space: normal; overflow-wrap: normal;">cheapest price</div></div></div></foreignObject><text x="610" y="44" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle">cheapest price</text></switch></g><ellipse cx="610" cy="100" rx="50" ry="20" fill="rgb(255, 255, 255)" stroke="rgb(0, 0, 0)" stroke-dasharray="3 3" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 98px; height: 1px; padding-top: 100px; margin-left: 561px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; white-space: normal; overflow-wrap: normal;">avg price</div></div></div></foreignObject><text x="610" y="104" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle">avg price</text></switch></g><ellipse cx="610" cy="160" rx="50" ry="20" fill="rgb(255, 255, 255)" stroke="rgb(0, 0, 0)" stroke-dasharray="3 3" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 98px; height: 1px; padding-top: 160px; margin-left: 561px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; white-space: normal; overflow-wrap: normal;">avg sale price</div></div></div></foreignObject><text x="610" y="164" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle">avg sale price</text></switch></g><ellipse cx="330" cy="340" rx="50" ry="20" fill="#f8cecc" stroke="#b85450" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 98px; height: 1px; padding-top: 340px; margin-left: 281px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; white-space: normal; overflow-wrap: normal;"><u>id</u></div></div></div></foreignObject><text x="330" y="344" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle">id</text></switch></g><ellipse cx="50" cy="20" rx="50" ry="20" fill="#f8cecc" stroke="#b85450" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 98px; height: 1px; padding-top: 20px; margin-left: 1px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; text-decoration: underline; white-space: normal; overflow-wrap: normal;">store name</div></div></div></foreignObject><text x="50" y="24" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle" text-decoration="underline">store name</text></switch></g><ellipse cx="410" cy="390" rx="50" ry="20" fill="rgb(255, 255, 255)" stroke="rgb(0, 0, 0)" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 98px; height: 1px; padding-top: 390px; margin-left: 361px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; white-space: normal; overflow-wrap: normal;">price</div></div></div></foreignObject><text x="410" y="394" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle">price</text></switch></g><ellipse cx="520" cy="390" rx="50" ry="20" fill="rgb(255, 255, 255)" stroke="rgb(0, 0, 0)" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 98px; height: 1px; padding-top: 390px; margin-left: 471px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; white-space: normal; overflow-wrap: normal;">timestamp</div></div></div></foreignObject><text x="520" y="394" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle">timestamp</text></switch></g><ellipse cx="580" cy="340" rx="50" ry="20" fill="rgb(255, 255, 255)" stroke="rgb(0, 0, 0)" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 98px; height: 1px; padding-top: 340px; margin-left: 531px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; white-space: normal; overflow-wrap: normal;">is_sale</div></div></div></foreignObject><text x="580" y="344" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle">is_sale</text></switch></g><path d="M 160 90 L 210 90" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="all"/><path d="M 355.03 96.31 L 354.97 83.29 L 330 89.9 Z" fill="rgb(0, 0, 0)" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="all"/><path d="M 481 60 L 486.5 39" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 460 170 L 520 200 L 460 230 L 400 200 Z" fill="#d5e8d4" stroke="#82b366" stroke-miterlimit="10" pointer-events="all"/><g transform="translate(-0.5 -0.5)"><switch><foreignObject pointer-events="none" width="100%" height="100%" requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility" style="overflow: visible; text-align: left;"><div xmlns="http://www.w3.org/1999/xhtml" style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 118px; height: 1px; padding-top: 200px; margin-left: 401px;"><div data-drawio-colors="color: rgb(0, 0, 0); " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 12px; font-family: Helvetica; color: rgb(0, 0, 0); line-height: 1.2; pointer-events: all; white-space: normal; overflow-wrap: normal;">Has</div></div></div></foreignObject><text x="460" y="204" fill="rgb(0, 0, 0)" font-family="Helvetica" font-size="12px" text-anchor="middle">Has</text></switch></g><path d="M 571.8 54.24 L 519.76 83.7" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 560.05 100.92 L 520 102" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 576.16 145.28 L 520 120" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 374.9 331.44 L 399.28 309.26" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 424.1 370.12 L 430 350" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 502.8 370.4 L 497.44 349.7" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 544.64 325.86 L 521.44 314.54" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 453.49 260.8 L 466.51 260.8 L 460 231 Z" fill="rgb(0, 0, 0)" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="all"/><path d="M 460 170 L 460 120" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="stroke"/><path d="M 461.81 250.04 L 461.81 290 M 457.81 290 L 457.81 250.04 M 457.81 290" fill="none" stroke="rgb(0, 0, 0)" stroke-miterlimit="10" pointer-events="all"/></g><switch><g requiredFeatures="http://www.w3.org/TR/SVG11/feature#Extensibility"/><a transform="translate(0,-5)" xlink:href="https://www.drawio.com/doc/faq/svg-export-text-problems" target="_blank"><text text-anchor="middle" font-size="10px" x="50%" y="100%">Text is not SVG - cannot display</text></a></switch></svg>
