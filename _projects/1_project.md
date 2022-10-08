---
layout: page
title: Codex
description: Natural Language Processing for Safety Critical Engineering Design
#img: assets/img/12.jpg
img: assets/img/codex.jpeg
importance: 1
category: work
---

Safety and other "ilities" are critically important in modern engineering systems. Meeting requirements represent a
significant fraction of development costs and schedules. Unlike other engineering disciplines, safety engineering does
not have computational tools to assist designers and analysts, especially for radically new concepts.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/aircraft.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/nuclear_reactor.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Examples of safety critical machinery: of the left, a series of new aircraft concepts from airbus. On the right, an experimental nuclear reactor.
</div>

Attempting to predict unknown hazards through physical simulation is not computationally feasible.

However, avoiding *repeating* accidents is.

Although every accident/incident is unique, **the patterns and mechanisms that produce them
 tend to repeat**, as can be seen in aircraft development (see [Jan Roskam's *Lessons Learned in Aircraft Design*](https://www.amazon.com/Lessons-Learned-Aircraft-Design-2007-05-15/dp/B01FKSGIO8)

A central issue is that historical data is often too large and complex to process by humans in order to extract relevant design information. The data relevant for safety and other ilities are usually stored as natural
language (i.e. accident reports, regulations, news articles, online reviews). Classical natural language processing
(NLP) has limited capability to process such texts. However, recent performance breakthroughs with Large Language
Models (LLMs) suggest that the application of NLP in Computer-Aided Design is within reach. A design knowledge
base could be built automatically from historical data (accident data/ regulatory documentation) and interacted with
intuitively. This scope of this research problem is too large to be treated in a single go:

The *Codex project* serves as a "toy problem" with the following objectives:

1. Demonstrate the application of current or even naive NLP techniques to a basic design problem
2. Set initial performance benchmarks using current/naive NLP approaches
3. Identify advantages and shortcomings of current NLP approaches in order to direct further research


**The Toy Problem**

Aircraft design problems make good case studies:
1. Aircraft are a typical illustration of complexe physical systems
2. The aeronautical industry is safety focused, and keeps track of "lessons learned" by intergrating them as safety requirements into the regulations
3. There are many regulations/norms that are freely available. In this case, we will use the European CS-22 norm, which covers motorglider design.

When designing or changing a part of an aircraft, every single *relevant* safety requirement must be selected from the regulations.

The "toy problem" then becomes the task of selecting relevant "lessons learned" (safety requirements) from a "knowledge base" (the CS-22 regulation)
for a given design problem. In this case, the design problem is a redesign of the aircraft's ailerons.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/ailerons.jpg" title="aileron image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Three View of an ASK-21 glider. Ailerons highlighted in red.
</div>
