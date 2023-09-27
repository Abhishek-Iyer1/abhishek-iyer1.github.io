---
title: "Lane Detection"
excerpt: "Attempting to solve the issue of correctly identifying your current driving lane with a high level of confidence. The approach is to segment the current driving lane by using both deep learning and classical approaches and weigh the limitations of each method in order to assist with automated driving. Training and test data includes varieties of daytime, road curvatures, types of road markings, and surronding environment for robust learning <br/><img src='/images/unet_predictions.png'>"
collection: portfolio
---

To reach a state where autonomous public transport and personal vehicles are reliably operating, there are still many challenges to be tackled. Here we take a look at the most fundamental problem in order to get from a start point to an end point autonomously - detecting the lane we need to be in. 

<style>
    .body {
        padding: 0;
        margin: 0;
    }
    .Parent {
        display: flex;
        flex-direction: row;
    } 
    .child1 {
        width: 40%;
        height: 75vh;
        /* background-color: green; */
        text-align: center;
        /* background-color: blue; */
    }
    .child2 {
        width: 60%;
        /* padding: 30px; */
        height: 75vh;
        /* border: green solid 5px; */
        margin-left: 24px;
        /* background-color: green; */
    }

    div {
        text-align: justify;
        text-justify: inter-word;
    }
</style>

### Demonstration and Discussion

<body>
    <div style="width: 70%; height: 70%; padding-top: 20px; padding-bottom: 20px; margin-left: 7.5vw;">
        <iframe width="340" height="191" src="https://www.youtube.com/embed/SW2Bq2x6ThA?autoplay=1&mute=1" title="Lane Segmentation | U-Net" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    </div>
    <div>
        <body>The aim of this task is to segment the current driving lane successfully. We employ a U-Net architecture with an encoder and a decoder which outputs the segmented mask, given an input image. After training the model locally, we find that it is able to predict very well on unseen images. The mean Intersection over Union (IoU) on 6.7k test images is approximately 92% which suggests that on most of the roads in out dataset, the model is able to perform sufficiently well. This is also reflected in the above video. </body>
    </div>
</body>

### Challenges and Future Work

<body>
    <div style="width: 70%; height: 70%; padding-top: 20px; padding-bottom: 20px; margin-left: 7.5vw;">
        <iframe width="1051" height="591" src="https://www.youtube.com/embed/qoTipmQLzLk?autoplay=1&mute=1" title="Lane Segmentation (Challenge)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    </div>
    <!-- Put second content here -->
    <p>On analyzing this particularly challenging video, we see multiple issues during prediction of the current lane. We notice that the U-Net model is only able to predict short distances accurately when the road contains extreme bends. It struggles to make continuous predictions when the road switches between shady and sunny. When the sun causes flashes of light, the onboard camera takes a second to adjust, overexposing the footage.</p>
    <p>We can make improvements in the future to tackle these issues. To name a few, we can augment the dataset with incorrectly exposed footage for robustness. Furthermore, we can incorporate a temporal block to the archtecture to predict changes in the road bend based on its recent history.</p>
</body>

<body><b>Techonologies: </b> Python, Jupyter Notebooks, Tensorflow, OpenCV, Numpy</body>

**GitHub Code Repository:** [Link](https://github.com/Abhishek-Iyer1/lane-detection/tree/main)
<!-- <body>
    <div class="Parent">
        <div class="child1">
            Put first column content here
            <h2> Lane Detection Challenge</h2>
            <div>
                <iframe width="1051" height="591" src="https://www.youtube.com/embed/qoTipmQLzLk?autoplay=1&mute=1" title="Lane Segmentation (Challenge)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
            </div>
        </div>
        <div class="child2">
            Put second content here
            <body>On analyzing the video, we see multiple issues during prediction of the current lane</body>
             <ul>
                <li>We notice that the U-Net model is only able to predict short distances accurately when the road contains extreme bends.</li>
                <li>It struggles to make continuous predictions when the road switches between shady and sunny.</li>
                <li>When in an odd position, the sun causes flashes of light, that the onboard camera takes a second to adjust to, overexposing the footage. This of course leads to incorrect predictions</li>
            </ul>
            <body>Future changes and improvements that can be made to tackle these issues</body>
            <ul>
                <li>Augmenting the current dataset with both overexposed and underexposed captures should contribute to the performance.</li>
                <li>Incorporating a heuristic which suggests when confidence is low, revert to the last high confidence output.</li>
                <li>Incorporate a temporal block to the architecture which can predict changes in the road based on its history</li>
            </ul>
        </div>
    </div>
</body> -->