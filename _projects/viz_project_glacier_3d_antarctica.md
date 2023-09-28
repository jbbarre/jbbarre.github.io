---
layout: page
title: Antarctica in 3D
description: <strong>Data Visualization</strong> <br> 3d map of Antarctica.
img: assets/img/portfolio_3d_antarctica.png
importance: 3
category: Data Viz - Cartography
---

Antarctica is the fifth largest continent and likely the last to be accurately mapped. The challenge in mapping the Earth on a flat surface, such as a screen or a book, is well known. The most commonly used maps of the Earth prioritize accurately representing the inhabited land areas, resulting in a compromised depiction of Antarctica. As a consequence, the shape of the continent is unrecognizable. This realization prompted the creation of an accurate 3D map of Antarctica. I utilized [Blender](https://jbbarre.github.io/projects/viz_project_blender/), a 3D computer graphics software, to create a numerical model of the continent that can be visualized in a web application. You can view the 3D model by accessing  <a href="https://ige-vis.univ-grenoble-alpes.fr/antarcticaStory/index3d.html"> here.</a>

<div class="row">
       <div class="col-sm mt-3 mt-md-0 text-center">
              {% include figure.html path="assets/img/antarctica_Projection_3857.png" title="" class="img-fluid rounded z-depth-1" %}
              <div class="caption">
                     Unreal representation of Antarctica using the Mercator projection (EPSG 3857).
              </div>
       </div>
       <div class="col-sm mt-3 mt-md-0 text-center">
              {% include figure.html path="assets/img/portfolio_3d_antarctica.png" title="" class="img-fluid rounded z-depth-1" %}
              <div class="caption">
                     Realistic 3D representation of Antarctica using the  Antarctic Polar Stereographic projection (EPSG 3031).
              </div>
       </div>

</div>
