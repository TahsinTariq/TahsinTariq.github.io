---
layout: post
title: Procedural Terrain Generation 
description: Using Perlin noise
image: assets/alternate_images/TG_front.png
nav-menu: false
main_tile: false
show_tile: true
date: 2020-04-15
permalink: terrain
categories: Code Procedural
tags: write
---

Creating a terrain manually for a game or just for visualization purposes is a really daunting task. Instead, a better way to do so is to programmatically generate it by passing some parameters to a code. Here, I discuss how to make a procedural terrain generator mostly using processing for python. This can also be done in any other language or game engine or 3D design software. I will be making a simple terrain using height maps for stylized purposes. But, first we need to understand how to generate height maps using perlin noise. 

Perlin noise is a procedurally generated noise texture developed by ken perlin. How perlin noise is generated using code is discussed thoroughly **[`here`](https://rtouti.github.io/graphics/perlin-noise-algorithm)**. I'll be using the built in noise function that generates perlin noise for processing. 

In order to render the terrain, we need some geometry. We can generate tile the plane with cubes, but that would look more like minecraft. We could choose randomly generated points. But due to the randomness, the points are too close to each other. 

<div class="grid">
	<img  src="{% link assets/alternate_images/random.png %}" alt="random points" data-position="center center" />
</div>

So, instead we use a different sort of random point generation called **[`Poisson Disc Sampling`](https://en.wikipedia.org/wiki/Supersampling#Poisson_disk)**. This generates random points at a given interval and thus making them more uniform.

Now if we triangulate the points,We should get a plane with enough geometry to offset using the generated height map. I go into some details on triangulation [`here`](https://tahsintariq.github.io/triangulation). The final result should look something like this (without the animation of course):

<div class="videoWrapper">
    <iframe
        src="https://tahsintariq.github.io/p5js/P5_Sketches/P5_Web_Collection/Delunay_triangulation"
        data-position="center center">
    </iframe>
</div>

Now we rotate the canvas on the y-axis so it looks more like a plane.

<div class="grid">
	<div style="width: 80%;margin:auto;">
		<img  src="{% link assets/images/random_plane.png %}" alt="random points" data-position="center center" />
	</div>
</div>

Now, using the generated height map, we offset the z-position of the points by the value corresponding to that x and y position in the height map. This gives us a stylized terrain.

<div class="grid">
	<div style="width: 80%;margin:auto;">
		<img  src="{% link assets/images/terrain.png %}" alt="random points" data-position="center center" />
	</div>
</div>

We can change the shape of this terrain by changing the noise using offsets. This can result in traversing through the terrain as if we were flying on top of it, or changing the entire topology of the terrain. It will depend on how the noise is being offset.

I've put the processing.py codes for this project [`here`](https://github.com/TahsinTariq/Processing/tree/master/Pycessing/Perlin/Terrain_generation)

Below are two different renders I've made using the same process. One with a half inverted color and the other colored according to the height of the points i.e. a topological height map.


<style>
	*.videoWrapper {
		position: relative;
		width:100%;
		padding-bottom: 56.25%; /* 16:9 */
		height: 0;
	}
	*.videoWrapper iframe {
		position: absolute;
		margin:auto;
		top: 0; bottom: 0;
		left: 0; right: 0;
		text-align: center;
		width: 90%;
		height: 90%;
	}
	*.grid{
	display: grid;
	place-items:center;
	/* width: 100%; */
    }
}
</style>

<style> iframe{ border: none; } </style>
<div class="videoWrapper">
    <iframe src="https://www.youtube.com/embed/kLhleR4t7LQ" data-position="center center">
    </iframe>
</div>
<div class="videoWrapper">
    <iframe src="https://www.youtube.com/embed/-vS37cZq3B8" data-position="center center">
    </iframe>
</div>
<!-- "https://www.youtube.com/embed/kLhleR4t7LQ"  -->
<!-- "https://www.youtube.com/embed/-vS37cZq3B8" -->