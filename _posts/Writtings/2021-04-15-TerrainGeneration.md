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

<!-- <p>Hollow Knight is a 2D Metroidvania action-adventure game, which takes place in Hollownest, a fictional ancient kingdom. The player controls an insect-like, silent, and nameless knight while exploring the underground world. The knight wields a nail, which is a cone-shaped sword, used both in combat and environmental interaction.</p> -->




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
	*.grid{
	display: grid;
	place-items:center;
	width: 100%;
    }
}
</style>

<style> iframe{ border: none; } </style>
<div class="videoWrapper grid" style="--aspect-ratio: 1 / 4;">
    <iframe src="https://www.youtube.com/embed/kLhleR4t7LQ" data-position="center center">
    </iframe>
</div>
<div class="videoWrapper" style="--aspect-ratio: 1 / 4;">
    <iframe src="https://www.youtube.com/embed/-vS37cZq3B8" data-position="center center">
    </iframe>
</div>
<!-- "https://www.youtube.com/embed/kLhleR4t7LQ"  -->
<!-- "https://www.youtube.com/embed/-vS37cZq3B8" -->