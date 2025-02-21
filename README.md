Input: Different views (JPGS) of an engineering part from a CAD model 
Output: Description of the feature/functionality of the part

I'm loading in CLIP (Contrastive-Learning Image Pre-training), which pairs images and texts in the same embedding space. 
I'm using FAISS (Facebook AI Similarity Search) to find similarity search between the image embeddings and the dataset of text embeddings, using zero-shot classification on CLIP. 

CLIP doesn't have the images it's trained on in memory, but it has the trained weights. It can map the dataset of text embeddings and find the closest match to the image. 
I've created a dataset of textual descriptions of various mechanical parts and turned them into embeddings along with the image embeddings. 
The text embedding(s)that are the closest in euclidean distance is what the model considers to be the best feature description(s) of the image.
