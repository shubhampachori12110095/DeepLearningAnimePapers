# DeepLearningAnimePapers
A list of papers and other resources on computer vision and deep learning with anime style images.
Contributions welcome!

## Contents
- [Anime Datasets](#anime-datsets)
- [Anime Papers](#anime-papers)
  - [Anime Colorization](#anime-colorization)
  - [Anime Generation](#anime-generation)
  - [Anime Inpainting](#anime-inpainting)
  - [Anime Datasets](#anime-datasets)
  - [Anime Pose Estimation](#anime-pose-estimation)
  - [Anime Sketch Simplification](#anime-sketch-simplifcation)
  - [Anime Misc](#anime-misc)
  - [Anime Non-Deep Learning](#anime-non-deep-learning)
- [General Papers](#general-papers)
  - [Image Colorization](#image-colorization)
  - [Image Generation](#image-generation)
  - [Image Inpainting](#image-inpainting)

# Anime Datasets
- 2000 anime/manga images with 2D pose annotations [[github]](https://github.com/dragonmeteor/AnimeDrawingsDataset) (Last updated June 10 2015)
- 109 manga volumes from the 1970s to 2010s [[link]](http://www.manga109.org/en/)
- 2.9+ million images database from Danbooru with tags [[link]](https://www.gwern.net/Danbooru2017) (Last updated Jan 23 2018)

# Anime Papers
## Anime Colorization
- Into the Colorful World of Webtoons: Through the Lens of Neural Networks [[semanticscholar]](https://www.semanticscholar.org/paper/Into-the-Colorful-World-of-Webtoons-Through-the-Le-Cinarel-Zhang/341d3329284158ba729dad88bbb59470655a97f8) (2017)
- Style Transfer for Anime Sketches with Enhanced Residual U-net and Auxiliary Classifier GAN [[arXiv]](https://arxiv.org/abs/1706.03319) (June 11 2017)
- cGAN-based Manga Colorization Using a Single Training Image [[arXiv]](https://arxiv.org/abs/1706.06918) (June 21 2017)

## Anime Generation
- Towards the Automatic Anime Characters Creation with Generative Adversarial Networks [[arXiv]](https://arxiv.org/abs/1708.05509) (August 18 2017)

## Anime Inpainting
- Joint Gap Detection and Inpainting of Line Drawings [[link]](http://openaccess.thecvf.com/content_cvpr_2017/papers/Sasaki_Joint_Gap_Detection_CVPR_2017_paper.pdf) (2017)

## Anime Datasets
- Manga109 Dataset and Creation of Metadata [[ACM]](https://dl.acm.org/citation.cfm?doid=3011549.3011551) (December 4 2016)

## Anime Pose Estimation
- Pose Estimation of Anime/Manga Characters: A Case for Synthetic Data [[ACM]](https://dl.acm.org/citation.cfm?id=3011552) (December 4 2016)

## Anime Sketch Simplification
- Sketch Simplification by Classifying Strokes [[IEEE]](http://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=7899777) (December 4 2016)

## Anime Misc
- Deep Extraction of Manga Structural Lines [[ACM]](https://dl.acm.org/citation.cfm?id=3073675) (July 2017)

## Anime Non-Deep Learning
- DrawFromDrawings: 2D Drawing Assistance via Stroke Interpolation with a Sketch Database [[PubMed]](https://www.ncbi.nlm.nih.gov/pubmed/27101610) (2016)
- Sketch-based Manga Retrieval using Manga109 Dataset [[SpringerLink]](https://link.springer.com/article/10.1007%2Fs11042-016-4020-z) (November 9 2016)
- Interactive Region Segmentation for Manga [[IEEE]](http://ieeexplore.ieee.org/document/7899993/) (December 4 2016)

# General Papers
## Image Colorization
- Real-Time User-Guided Image Colorization with Learned Deep Priors [[arXiv]](https://arxiv.org/abs/1705.02999) (May 8 2017)

## Image Generation
- StackGAN++: Realistic Image Synthesis with Stacked Generative Adversarial Networks [[arXiv]](https://arxiv.org/abs/1710.10916) (October 19 2017) [[original pytorch implementation]](https://github.com/hanzhanggit/StackGAN-v2)
- Progressive Growing of GANs for Improved Quality, Stability, and Variation [[arXiv]](https://arxiv.org/abs/1710.10196) (October 27 2017) [[original theano/lasagne implementation]](https://github.com/tkarras/progressive_growing_of_gans)

## Image Inpainting
Title | Contributions | Shortcomings | Maximum Input Size | Code?
--- | --- | --- | --- | ---
Semantic Image Inpainting with Deep Generative Models [[arXiv]](https://arxiv.org/abs/1607.07539) (July 26 2016) | <ul><li>Missing content infered by searching for closest encoding of the corrupted image in the latent image manifold.</li></ul> | <ul><li>No end to end training.</li><li>IMHO, generating images is harder than inpainting images because with inpainting, there is always ground truth present. So solving inpainting by converting it to the harder problem of generating images is not the way to go.</li></ul>
Globally and Locally Consistent Image Completion [[link]](http://hi.cs.waseda.ac.jp/~iizuka/projects/completion/en/) (2017) | <ul><li>Dilated convolutions</li><li>2 discriminators: one local discriminator for the completed region and one global discriminator for whole image</li></ul> | <ul><li>Long training time.</li><li>Poisson blending needed.</li><li>Complex training process. Completion network is trained, then the completion network is fixed and discriminators are trained, then finally both are trained.</li></ul> | 256 x 256 x 3 | Soon
Image Inpainting using Multi-Scale Feature Image Translation [[arXiv]](https://arxiv.org/abs/1711.08590) (November 23 2017) |
Context-Aware Semantic Inpainting [[arXiv]](https://arxiv.org/abs/1712.07778) (December 21 2017) |
Light-weight pixel context encoders for image inpainting [[arXiv]](https://arxiv.org/abs/1801.05585) (January 17 2018)
High Resolution Face Completion with Multiple Controllable Attributes via Fully End-to-End Progressive Generative Adversarial Networks [[arXiv]](https://arxiv.org/abs/1801.07632v1) (January 23 2018) | <ul><li>Conditioned on facial attributes.</li><li>Progressive growing of GANs.</li><li>Three new losses: attribute, feature, and boundary.</li></ul> | <ul><li>Fails to learn low level skin features.</li><li>Long training time.</li></ul> | 1024 x 1024 x 3 | Soon
Deep Structured Energy-Based Image Inpainting [[arXiv]](https://arxiv.org/abs/1801.07939) (January 24 2018) |