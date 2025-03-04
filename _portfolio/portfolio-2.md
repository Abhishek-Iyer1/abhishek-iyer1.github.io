---
title: "Figma Creative Assistant"
excerpt: "During my time at Aalto University, one of my main tasks was researching and developing a tool to assist UI designers explore color harmony. We used deep learning saliency models to extract colors from the focal points to build a palette around, which was extended using Monte Carlo Tree Search. The tool employed multiple assignment algorithms and heuristics in order to ensure light-dark variations, minimum contrast levels for accessibility, and a thorough user study. The tool was created as a plugin on the popular designing platform - Figma.<br/><img src='/images/colorize_sample.png'>"
collection: portfolio
---
<style>
    .special {
        text-align: justify;
        text-justify: inter-word;
    }
</style>

### Demonstration and Discussion

<div style="width: 70%; height: 70%; padding-top: 20px; padding-bottom: 20px; margin-left: 7.5vw;">
    <iframe width="1051" height="591" src="https://www.youtube.com/embed/f_V3fEX8f7s?autoplay=1&mute=1" title="Figma Creative Assistant - An Interactive Coloring Tool" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

<p class="special">A crucial step of the designing process is Rapid Prototyping. Building high fidelity mockups quickly can become tedious. The plugin is designed with this in mind and aims to be a faithful creative assistant to the designer. It allows for rapid exploration of color palettes inspired from a focal object, often times a product in marketing material. It even allows modification of generated color palettes in order to quickly generate finer variations in the UI. We believe the designer should always be in control and to that extent, while the plugin uses Artificial Intelligence, algorithms and heuristics for separate steps of the coloring process, the designer can guide the plugin to create their desired output. This significantly reduces the time of the rapid prototyping stage.</p>

The different stages of this process are as follows:
<ul>
    <li class="special"><b>Color Extraction</b>: Automatically detecting the focal image, and using an enhanced Median Color Quantization algorithm to pick key colors.</li>
    <li class="special"><b>Palette Extension</b>: Using Monte Carlo Tree Search and Gaussian Mixture Models, we extend the palette with missing colors to create a harmony of complementing colors.</li>
    <li class="special"><b>Color Assignment</b>: Assigning the colors from the palette to different layers of the UI design.</li>
    <li class="special"><b>Ensuring Visual Coherence</b>: Checking certain metrics such as contrast, warm-cool combinations, luminance variations to ensure an appealing end result.</li>
</ul>

<body><b>Technologies: </b> Python, Pytorch, Numpy, TypeScript, Figma API</body>

**Publication:** [Link](https:abhishek-iyer1.github.io/publication/2023-cocolor-interactive-exploration-of-color-designs)\
**GitHub Code Repository:** Private Repository