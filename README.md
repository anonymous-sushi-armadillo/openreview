This repository contains figures relevant to the discussion on OpenReview. 

The curve showing the effects of step size on FGSM adversarial training on CIFAR10 
can be found [here](https://github.com/anonymous-sushi-armadillo/openreview/blob/master/step_size_cifar10.pdf). 
Note that the the error bars represent standard deviation over 3 different random seeds. 

A table containing the performance of R+FGSM as done by 
[Ensemble Adversarial Training](https://openreview.net/forum?id=rkZvSe-RZ) is in the following table, 
with several tweaks showing the effect of various choices in the adversary. The results are over 10 random seeds.
Note that using a uniform initialization adds the greatest improvement to the original R+FGSM attack, while 
a full step size doesn't seem to help on its own. Implementing both of these improvements results in the form of 
FGSM adversarial training presented in our paper. 

| Attack                  | Mean PGD accuracy | Standard deviation |
| ----------------------- |:-----------------:| ------------------:|
| R+FGSM                  | 34.58%            | 36.06  |
| R+FGSM (uniform init)   | 72.92%            | 10.40  |
| R+FGSM (full step size) | 26.53%            | 32.48  |
| Uniform + full (ours)   | 86.21%            | 00.75  |
