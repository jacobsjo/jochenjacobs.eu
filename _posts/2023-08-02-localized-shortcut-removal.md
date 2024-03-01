---
layout: post
title: "Removing localized shortcuts from training data"
tagline: "CVPR Workshop paper"
categories:
  - blog
  - project
author: "Jochen Jacobs"
---
For my master’s thesis, I have researched the issue of "shortcuts" in training data. Imagine you want to train a classification network on a set of training images, but all images of class A have watermarks while images of class B doesn't. In that case, the training makes the network pay attention to the existence of a watermark to differentiate the classes, but fails to generalize to the case without these watermarks. When this network is then deployed in the real-world, it is not able to do its job.

To solve this problem, I have employed an image-to-image network, called *lens*, that is put in front of the classification network and is trained adversarial to make it harder for the classification network to classify the images. An additional "reproduction loss", i.e. a penalty for editing the image too much, ensures the *lens* can only remove shortcuts.

The first row of the below image shows an example training dataset of grayscale images of goose and flamingos, where the flamingo images have watermarks added to them. The second row shows the output of the lens. As you can see, the lens is partially removing the watermarks, and partially adding watermarks to the goose images. This makes the subsequent classification task much harder, such that a trained network doesn't use the watermarks as clues.

![Lens removing shortcuts](/assets/blog_assets/localized-shortcut-removal/example.png)
&nbsp;

Full details about this research can be found in the published CVPR-Workshops paper:
> Nicolas M. Müller\*, **Jochen Jacobs**\*, Jennifer Williams, and Konstantin Böttinger. "Localized Shortcut Removal," 2023 IEEE/CVF Conference on Computer Vision and Pattern Recognition Workshops (CVPRW), Vancouver, BC, Canada, 2023, pp. 3721-3725, DOI:[10.1109/CVPRW59228.2023.00382](https://doi.org/10.1109/CVPRW59228.2023.00382), avaliable [at the Computer Vision Foundation](https://openaccess.thecvf.com/content/CVPR2023W/XAI4CV/html/Muller_Localized_Shortcut_Removal_CVPRW_2023_paper.html)
>
> *equal contribution

A more detailed version is available on ArXiv:
> Nicolas M. Müller\*, **Jochen Jacobs**\*, Jennifer Williams, and Konstantin Böttinger. "Shortcut Removal for Improved OOD-Generalization," [arXiv:2211.15510 [cs.CV]](arXiv:2211.15510 [cs.CV])
>
> *equal contribution
