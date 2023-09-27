---
title: "Marine Search and Rescue"
excerpt: "Developing our own object detection models to aid in detecting, counting, and tracking people at sea during search and rescue missions. Further differentiation between floaters and rescue members can be made. Can extend this pronlem to tackle multi object tracking so even temporal data can be analyzed. <br/><img src='/images/object_detection_pipeline.png'>"
collection: portfolio
---

<style>
    .special {
        text-align: justify;
        text-justify: inter-word;
    }
</style>

<p class="special">Search and rescue missions out in the ocean can be very complex, with the number of people in need of help ranging to hundreds at a time. It can become especially challenging to keep count of the people needing help in such a dynamic environment.<p>

<h3>Demonstration and Discussion</h3>

<div style="width: 70%; height: 70%; padding-top: 20px; padding-bottom: 20px; margin-left: 7.5vw;">
    <img src="/images/predictions.png" alt="Faster-RCNN Predictions">
</div>

<p class="special"> We aim to use a popular architecture for object detection, Faster-RCNN, to be able to recognize humans in the scene and classify them in one of six categories. The model uses a ResNet-50 backbone which condenses the input image down into a feature map which is the basis for generating proposals. There is a classifier head, regression head, and confidence head which predict the category of the object, the bounding box and its offsets, and the confidence of the initial classifcation respectively. Using this approach we are able to count quite accurately the number of humans in the scene and further split it into "Rescued" and "To be rescued".</p>

<h3>Challenges and Future Work</h3>

<p class="special"> The model struggles to make accurate predictions when the humans in the scene are only a few pixels big. We can experiment with the ratios and scales of the anchor boxes generated in the RPN to combat this particular issue and use a deeper backbone which has been finetuned on this dataset. The problem statement can be taken one step further from object detection to multi-object tracking. In this we would assign IDs to all the humans in the scenes and could even store their temporal movement to predict their trajectories and point out other risks. A good starting point would be to see the performance of a model such as Deep SORT.</p>

<body><b>Techonologies: </b> Python, PyTorch, OpenCV, Numpy</body>
<br>
<body><b>GitHub Code Repository</b>: <a href="https://github.com/Abhishek-Iyer1/marine-search-and-rescue/tree/main">Link</a>