
<center><span style="font-size:120%">CHARACTERIZING SIGNAL PROPAGATION TO CLOSE THE PERFORMANCE GAP IN UNNORMALIZED RESNETS</span></center>

<div style="text-align:right">Department of Artificial Intelligence<br>202224205 HyunSeok Jung</div>

<span style="font-size:110%">1. Main Contribution</span>

<img src='https://user-images.githubusercontent.com/78655692/172666321-ebf60f21-aa44-45f2-8f73-cffa49eb2481.png' width=800 height=180>

- Authors seek to the architecture for training deep Resnet without normalization layers, which achieve test accuracy competitive with Effinet SOTA.
  1. They use signal propagation plots (SPP) which shows the plot the following hidden activation statistics at the output of each residual block.
  2. They introduces two scalar values $\alpha, \beta$ to mimic effect of batch normalization which downscales the hidden activations on the residual branch.
  3. They introduces scaled weight standardization to prevent the emergence of a mean shift.

<span style="font-size:110%">2. Main Experimental results </span>


![image](https://user-images.githubusercontent.com/78655692/172668818-95f724af-1066-4d45-bbb3-ea0ee7061c54.png)

- Introducing learnable scalar values and scaled weight standardization, nfnet replaced the function of batch normalization, such as being able to stack layers deep, showing high accuracy as experimental results.
- The performance is maintained even when batch size is small in nf-resnet.

<span style="font-size:110%">3. Unknown or undescribed weak point </span>

- Experimental results from other models were shown in the appendix, with the top-1 accuracy of the EfficientNet-B5 being 83.1%, while NF-ResNets was 79.6%, which still showed insufficient performance compared to the SOTA.
- They showed that NF-ResNets works well when the batch size is small, but the paper does not reveal what performance it shows when the batch size exceeds 1024.


<span style="font-size:110%">4. The reason Why I chose this paper. </span>

- I am currently interested in distributed deep learning when use large scale, and I am thinking about how to reduce communication costs. In the meantime, I found that batch normalization is the most computationally expensive, and as a result of thinking I found this paper.