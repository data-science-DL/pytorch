
<center><span style="font-size:250%">Mid-term_report</span></center>

<br>
<br>

<div style="text-align:right">202224205 HyunSeok Jung</div>

<br><br>

- **Alexnet** : AlexNet was the first large-scale CNN and was used to win the ImageNet Large Scale Visual Recognition Challenge (ILSVRC) in 2012.
  - pros : It was the first architecture that employed max-pooling layers, ReLu activation functions, and dropout for the 3 enormous linear layers.
  - cons : it cannot stack more layers due to the problem of vanishing problems.
- **VGG** : It was the first study that provided undeniable evidence that simply adding more layers increases the performance.
  - pros : they use only 3x3 kernels, decrease the number of parameters
    - Block was used to avoid the vanishing gradient problem.
  - cons : Memory usage is high.
- **Inception** : it uses convolutions of different kernel sizes (5×5, 3×3 , 1×1) to capture details at multiple scales
  - pros :  It achieves deeper architecture by employing a number of distinct techniques, including 1×1 convolution and global average pooling.
  - cons : GoogleNet CNN architecture(=inception) is computationally expensive.
- **ResNet** : Use residual networks, such as skip connections
  - pros : The deep residual nets can easily enjoy accuracy gains from greatly increased depth, producing results substantially better than previous networks.
  - cons : circuit complexity theory, Diminishing feature reuse
- **Wide-ResNet** : Existing ResNet papers are studies that have been keen on deep building but have argued that what is important is residual widely, not depth.
  - **pros** : Enables parallel processing to increase computational efficiency.
  - **cons** : It is difficult to see significant improvements in performance compared to existing models.
- **ResNext** : Adopt the iterative layer strategy of VGG/ResNet while utilizing the split-transform-merge strategy, an easy and extensible method using the cardinality method.
  - **pros** : Demonstrate better performance with increasing cardinality.
  - **cons** : It is difficult to see significant improvements in performance compared to existing models.
- **MobileNet** : MobileNets are CNNs that can be fit on a mobile device to classify images or detect objects with low latency. 
  - **pros** : They can reduce computational costs also parameters
  - **cons** : Looking at the evaluation results in Object Detection (the numbers 300 and 600 in SSD and Fast R-CNN correspond to the size of the input), the mAP is somewhat inferior.
- **EfficientNet** : search for optimal set of compound scaling factors given a compute budget
  - **pros** : efficient training using small parameters and small flops
  - **cons** : slow latency