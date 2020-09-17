---
layout: post
title: Intelligent Agents
description: Posting my assignment here instead of going through the trouble of making a PDF
# image: assets/images/HK_Sisters_of_Battle_01.png
nav-menu: false
main_tile: true
show_tile: true
---
In our final class of Introduction to AI, we were asked to write about which agent type we liked or preferred most out of the five mentioned by [Russell & Norvig](https://en.wikipedia.org/wiki/Intelligent_agent#CITEREFRussellNorvig2003) in their book. Here I discuss about it.

## The agent types:
As stated earlier, there are 5 types of agents.

* Simple reflex agent
* Model based reflex agent
* Goal based
* Utility based
* Learning agent

## Preferred agent:
Among these 5, I prefer the learning agent due to it's generalization of the concepts of the other 4 agents. To explain why, we first need to look at how the agents works.

<style>
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
</style>

<figure>
<div style="display:flex">
    <div style="flex:1;padding:0 1% 0 0">    
        <img src = "{% link assets/alternate_images/LearningDiagram2.png %}" alt = "Image No.1">
    </div>
    <div style="flex:1; padding:0 1% 0 0">
        <img src = "{% link assets/alternate_images/LearningDiagram3.png %}" alt = "Image No.2">
    </div>
    </div>
    <div>
    <p></p>
    </div>
    <div style="display:flex">
    <div style="flex:1;padding:0 1% 0 0">    
        <img src = "{% link assets/alternate_images/LearningDiagram4.png %}" alt = "Image No.3">
    </div>
    <div style="flex:1; padding:0 1% 0 0">
        <img src = "{% link assets/alternate_images/LearningDiagram5.png %}" alt = "Image No.4">
    </div>
</div>
<figcaption align="center"><i>Fig.1 - Simple reflex, model, goal and utility based agents.</i></figcaption>
</figure>

<div>
<p></p>
</div>
<div style="text-align: justify">
Here it can be seen that the performance of the simple reflex agent is largely dependent on the condition-action rules that are predefined. It has no sense of history and the consequences of it's actions. The downside to this is that the agent, while can perform well in an extremely constrained (i.e fully observable) environment, will fail to do so in partially observable conditions.
</div>

<div>
<p></p>
</div>

<div style="text-align: justify">
In order to solve this problem, the model, goal and utility based agents have been developed. They are provided with, as their names suggest, model, goal and utility. When a model is provided, the agent has the ability to sustain a percept history which helps it understand how the environment functions around it. And yet, it cannot make a guess on how to act accordingly in all possible scenario. To build on top of this, the agent is further given a goal. This helps it avoid undesirable situations and steer towards better results. but this too has it's flaws as the results achieved might not always be the optimal result. Thus the agent is provided with utility. This ensures that the results provided by the agent is optimal. But here we face another problem. and that is a way to find the utility-maximizing course of action. Perfect rationality is often very difficult if not unachievable in a real world environment due to it's unpredictability and the limitations with computational complexity.
</div>
So, now lets look what the learning agent has to offer.
<div>
<p></p>
</div>

<figure>
    <div style="display:flex">
        <div style="flex:1;">
            <div style="flex:1; padding:0 3% 0 0;">
                <img 
                    style="display: block;margin-left: auto;margin-right: auto;width=10%;" 
                    src="{% link assets/images/LearningDiagram1.png %}" 
                    alt="Learning Agent"
                >
            </div>
        </div>
    </div>
    <figcaption align="center"><i>Fig.2 - A general learning agent.</i></figcaption>
</figure>

<div>
<p></p>
</div>

## Why I prefer it to others:

<div style="text-align: justify">
Learning agents can operate in initially unknown conditions and improve over time. This can be attributed to the four basic components as seen in fig.2

* <b>Critic </b>: This tells the agent whether it's current course of action is leading to an optimal outcome or not. So, it find the difference between the optimal actions and help modify the percept model with respect to achieving it's goals so that the learning agent can update itself.
* <b>Learning element </b>: The learning element takes the feedback from the critic and determines how the performance element should evaluate to some action in an environment. It in a way, acts like the condition-action rules as seen in a simple reflex agent where the rules for conditions and actions are updated from the critic.
* <b>Performance element </b>: This is responsible for selecting the actions. I think of it as equivalent to the utility function because it's job is to choose the optimal out of all possible solutions. But it can also be thought of as the percept of reward or penalty for a certain set of actions.
* <b>Problem Generator </b>: This is a bit different from the rest of the agents as it introduces a new concept. The problem generator creates some variations in the choices and suggests experiments by identifying possible improvements. These new experiences help the agent discover better actions.
<div>
<p></p>
</div>
<p>
Looking at the properties of the learning agent, it's easy to see how it encapsulates the other four agents and even expands upon them to perform better.
</p>
</div>
