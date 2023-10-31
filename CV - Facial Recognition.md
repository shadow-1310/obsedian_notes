
#### Papers
- DeepFace Paper, Taigman et. al
- FaceNet, Schroff et. al

Facial Verification vs Facial Recognition
- facial verification is 1:1
	- here we give one input image and an id and check if that matches
- recognition is 1:k
	- here we give one input image and check if that matches a database of k images


### One shot learning
- if we have 4 people, then we can train a cnn model with softmax output of 5 class, (4 person and 1 NOTA)
- but every time a new person joins we have to retrain the network, which is not a good idea
- so we make a similarity learning function
- d(img1, img2) = degree of difference between images


### Siamese Network
- apply cnn to different images to get image representation as a vector
- images are not stored on the database, instead encodings calculated by CNN are stored. this saves computation time

#### Triplet Loss
- anchor - target person
- positive - same person as anchor
- negative - different person than anchor
- d(A,P) - d(A,N) <= 0
	- it has a flaw that by making each image vector 0 , it can satisfy the equation
	- so we use a margin -alpha on the right hand side
	- d(A,P) - d(A,N) + alpha <= 0
- can't choose triplet randomly, because for some cases the equation will be easily satisfied and the algorithm won't learn
	- choose triplet that are hard to train on, such that (A,P) and (A, N)  are very similar.

- it is used for facial recognition
- triplet loss
