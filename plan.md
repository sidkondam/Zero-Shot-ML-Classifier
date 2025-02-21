Input: Different views (JPEGS) of an engineering part from a CAD model 
Output: Description of the feature/functionality of the part

Plan: 
We are loading in CLIP (Contrastive-Learning Image Pre-training), which pairs images and texts in the same embedding space. 

We are using FAISS to find similarity search between the image embeddings and the dataset of text embeddings, using zero-shot classification on CLIP. 

CLIP doesn't have the images it's trained on in memory, but actually the trained weights. It can map the dataset of text embeddings and find the closest match to the image. 
