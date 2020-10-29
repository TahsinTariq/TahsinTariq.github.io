---
layout: post
title: A Study on Triangulation
description: A small demonstration of my love of Triangulating anything and everything
image: assets/images/shaan_triangulated.jpg
nav-menu: false
main_tile: false
---

</style>
<p>In geometry, triangulation is a partition of a geometric object into simplexes. On a plane, these are triangles.</p>

### Delaunay triangulation algorithm
Let's introduce some constrains:
* Let a geometric object be described by a set of points on the $ S $ plane. Triangulation for a finite set of points $ S $ is the problem of triangulation of the convex hull $ CH (S) $, which covers all points of the set $ S $. 
* Segments of straight lines cannot intersect, but can meet at common points belonging to the set $ S $. We will call these segments <b> edges </b>.
* A set of points is <b> circular </b> if there is a circle on which all the points of the set lie. For this set of points, this circle will be circumscribed. For a triangle, this circle will pass through all three of its non-collinear vertices.
* The circle will be <b> free of points </b> if there are no points from the set $ S $ inside the circle.
* Triangulation for a set of points $ S $ - <b> Delaunay triangulation </b> if each circumcircle for each triangle is free of points.

Two conclusions can be drawn from these definitions:
* For triangulation to exist, there must be at least three non-collinear points in the $ S $ set.
* For the Delaunay triangulation to be unique, it is necessary that no 4 points from the set $ S $ lie on the same circumcircle.

<p>I've tried various ways to use the triangulation algorithm in generating beautiful patterns.</p>

<!-- <div class="videoWrapper">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/r9JzMWXTGwQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
<p> -->

<style>
	*.videoWrapper {
		position: relative;
		padding-bottom: 56.25%; /* 16:9 */
		height: 0;
	}
	*.videoWrapper iframe {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
	}
}
</style>
<style> iframe{ border: none; } </style>
<div class="videoWrapper" style="--aspect-ratio: 2 / 4;">
    <iframe 
        src="https://tahsintariq.github.io/p5js/P5_Sketches/P5_Web_Collection/Delunay_triangulation"
        data-position="center center">
    </iframe>
</div>
<p>
</p>

<!-- <div class="videoWrapper" style="--aspect-ratio: 3 / 4;">
<iframe src="https://www.youtube.com/embed/fY4qkfjJo6A" alt="" data-position="center center" /></iframe>
</div> -->
