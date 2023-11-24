# Harm Detection in Memes
## About
There have been many isolated studies in detection of hate speech , misinformation and
offensive content. Given the multimodality of the memes it is necessary that the images and
text be considered together to identify whether a meme is harmful or not. To achieve this
Shraman Pramanic et. al. came up with the MOMENTA (MultimOdal framework for
detecting hateful MemEs aNd Their tArgets) Architecture. Under this architecture they
incorporated fusion techniques along with state of the art CLIP (Contrastive Language Image
Pre-Training) to not only identify whether the meme is harmful or not but also determine the
target of the meme.

We took inspiration from MOMENTA and introduced several changes to it, such as extracting best label,
improving on the various NLP and CV models used, and achieved a very significant increase in accuracy
(nearly 81% from the existing 77%) on the Harm-C dataset.

Here is a visual representation of our model:
![image QOP8E2](https://github.com/omkmorendha/Harm-meme-detection/assets/17925053/f1a53886-0e62-4303-a8ad-fdf4519b2fe3)

Here are the various sub-models we used for our model
1. Computer Vision
     1. VGG-16
     2. VGG-19
     3. DenseNET
     4. YOLO
     5. ResNet
     6. Visual Transformer
2. NLP
    1. MPNet
    2. DistilRoBERTa
    3. MiniLM  
3. CLIP (Both Text and Image)
   
## Results 
We tweaked around the original implementation of MOMENTA and introduced newer and better CV and NLP models due to which we achieved a significant improvement over the original model. We also extracted the “best-label” for each image that helped us get a more in depthful insight into each image. Due to these changes, our best model outperformed MOMENTA in all baselines but one.

Results Table:

![image](https://github.com/omkmorendha/Harm-meme-detection/assets/17925053/8b87d3fe-1313-4f88-9d1b-30f5b4744731)
