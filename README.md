
# Defect detection with an Adversarial Autoencoder

## Introduction

Defection detection is of great importance for mass production. Phone screens are inspected to ensure there are no scratchs on them. Solar cells are examed and products with cracks are tossed away. Metal  bearings need careful examination because cracks and holes can severely damage mechanical performance.

Traditional optical defection detection relies on hand-engineered filters and kernels to extract the features about certain type of defects. This method usually require lots of domain knowledge and often suffer from low signal-to-noise ratio. 

Supervised machine learning methods have been sucessfully applied to the problem and reached unparallel accuracy and effeciency. However, supervised machine learning models demand a large amount of human annotated data. In the meantime, the number of defective samples is usually limited, which raises the data imbalancement problem.

This project describes a unsupervised defect detection method by using an adversarial autoencoder to reconstruct the normal samples. After training, the generator is asked to reconstruct defective samples. Because the model is purely trained on normal samples, it does not process the knowledge or experience to reconstruct defects. The defects will be removed in the reconstructed image. A residual image can be obtained by simply subtracting the defect image from the reconstructed image, where defects can be clearly identified and located.

## Algorithm illustration

Train with normal samples.
<p align="left">
  <img src="https://github.com/tojunesa/defect-detection-with-GAN/blob/main/img/algorithm%20illustration%201.png" width="600"/>
</p>

Reconstruct defective samples and obtain residual images.
<p align="left">
  <img src="https://github.com/tojunesa/defect-detection-with-GAN/blob/main/img/algorithm%20illustration%202.png" width="600"/>
</p>


## Results

![Example 1](https://github.com/tojunesa/defect-detection-with-GAN/blob/main/img/example1.png)

![Example 2](https://github.com/tojunesa/defect-detection-with-GAN/blob/main/img/example2.png)

![Example 3](https://github.com/tojunesa/defect-detection-with-GAN/blob/main/img/example3.png)
