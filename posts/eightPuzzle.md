---
layout: post
title:  Eight-Puzzle Game
description: A playable Javascript implementation of the classical 8-puzzle game that can also be solved using AI if you're stuck
nav-menu: false
main_tile: false
show_tile: true
---

This is a JavaScript implementation of the 8-puzzle game.

Use the following keys to control the blank tile  
<div style="display:flex">
    <div style="flex:1;padding:0 1% 0 0">
        <h1>
            <div ALIGN=Center>
                ↑
            </div>
            <div ALIGN=Center>
                ←  ↓  →
            </div>
        </h1>
    </div>
    <div style="flex:1;padding:0 1% 0 0">
        <h1>
            <div ALIGN=Center>
                W
            </div>
            <div ALIGN=Center>
                A  S  D
            </div>
        </h1>
    </div>
</div>

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
        src="https://tahsintariq.github.io/p5js/P5_Sketches/P5_Web_Collection/EightPuzzle"
        data-position="center center">
    </iframe>
</div>



