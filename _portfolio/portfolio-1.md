---
title: "Design.AI - Ensuring brand consistency"
excerpt: "While at Design.AI, I was one of the core developers on making a multi platform AI backed tool to assist businesses in digitizing their brand guidelines and providing all designers instant evaluation on their designs with respect to the company's brand guidelines. We also digitized Google's Material Design 3 design system used by most freelancers. The plugin also offered suggestions for fixing violated guidelines, in addition to evaluating and fixing a few of the WCAG accessibility guidelines. Additionally, we provided a custom dashboard for managers to track team progress, improvement in efficiency, and business expenses saved. We further partnered with leading companies such as H&M and Kone to gain insights from their design teams on the Beta version of the tool. <br/><img src='/images/designai_features.png'>"
collection: portfolio
---
 

### Demonstration and Discussion
<style>
    .special {
        text-align: justify;
        text-justify: inter-word;
    }
</style>

<div style="width: 70%; height: 70%; padding-top: 20px; padding-bottom: 20px; margin-left: 7.5vw;">
    <iframe width="1051" height="591" src="https://www.youtube.com/embed/DX_AdrazHKE?autoplay=1&mute=1" title="Design.AI Demo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>

<p class="special">Ensuring consistency in brand image and levels of accessibility can become an inefficient task with a lot of iteration over designs and wasted designer time in pixel pushing. Design.AI was created as a tool to combat these issues, allowing designers to spend their time on making creative decisions rather than tedious labour like making pixel perfect designs or reading extensive guidelines about their employer's brand image.</p>

The different features offered by Design.AI are as follows:
<ul>
    <li class="special"><b>Design Review</b>: Comparing the current design with the selected design system (digitized brand guidelines). Reporting violations, suggesting fixes, calculating compliance score, and measuring other key metrics.</li>
    <li class="special"><b>Design Evaluation</b>: Calculating heatmaps and gazeplots from architectures developed in conjunction with the Computational Research Lab at Aalto University in order to optimize the UI to better grab the end user's attention.</li>
    <li class="special"><b>Accessibility</b>: Reporting all accessibility conflicts such as contrast issues between any two layers in extremely complex designs in real-time. Suggests fixes according to the Web Content Accessibility Guidelines (WCAG) 2.0.</li>
    <li class="special"><b>Reports and Dashboard</b>: Reflecting all the data as concise reports in a dashboard website for design leads, and managers. Provides a useful synopsis of open and closed issues and reflects month on month KPIs such as compliance and operational costs saved.</li>
</ul>

<p class="special">We have developed this tool mainly in conjunction with the Figma API as Figma is the first application the plugin is deployed on. In creating several of the above listed features, a lot of new technologies were researched and developed, such as the deep learning models created for Design Evaluation. Deep learning models such as Large Language Models (LLMs), gaze estimation models, and Convolutional Neural Network (CNN) classifiers are a few of the key technologies used. Furthermore, data structures like graphs and trees were primarily used with modified algorithms for evaluating the design during Design Review and evaluating Accessibility. All the important company data including digitized guidelines, designers, team leads, and important KPIs were stored in multiple relational databases.</p>

<p class="special">Professional UI/UX designers and their feedback has been integral in creating this tool. It has been an iterative process to ensure that we are actually able to deliver the value we believe this tool will provide. Multinational brands like H&M and Kone have taken interest in this tool. The company website can be found below.</p>


<body><b>Technologies: </b> Python, Pytorch, TypeScript, React, SQL, Kubernetes, Docker, Microsoft Azure, HTML, CSS, Figma API</body>

**Company Website:** [Link](https://designai.aalto.fi)\
**GitHub Code Repository:** Private Repository
