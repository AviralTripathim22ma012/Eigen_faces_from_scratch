## Implementation:
Eigenfaces is a facial recognition algorithm that is based on the 
principal component analysis (PCA) technique.
 The first few eigenvectors indicate the most crucial features of 
the faces in the training set, such as eyes, nose, and mouth are 
just a few examples 
 To recognize a new face, the algorithm projects the image onto 
the eigenspace spanned by the eigenfaces and computes the 
distance between the projection and the projections of the 
training images. 
 The closest match in the training set is then used to identify the 
person in the new image.
It is computationally effective and only requires a limited amount of 
training photos, Eigenfaces is a well-liked method for recognising faces. 
However, it has some drawbacks, including sensitivity to lighting.

## Qualitative analysis:
Visual inspection: every eigen face captures a specific facial 
detail, like some may give importance to eyes, some to nose, some to 
lips, etc., and give prominence to it 
In the above case as well we can observe that in the case of k= 5, the 3rd
eigen face gives prominence to hairs 

## Quantitative analysis:
Reconstruction error: generally the reconstruction error 
decreases with the increase in the value of K (top K eigen faces used for 
reconstruction), as more the number of eigen faces used, more the 
details and features captured, better the reconstruction
But in my case we can observe that the reconstruction error remains 
constant when increasing k, the main reasons for this could be:
Insufficient number of training samples: If the number of training 
samples used to derive the eigenfaces is too small (11 images), 
the eigenfaces may not capture enough variation in the facial 
images, leading to a similar reconstruction error for different 
values of k. 
Normalization of data: we should normalize the data before 
applying the PCA algorithm to derive the eigenfaces. If the data is 
not normalized, the resulting eigenfaces may not be optimal, 
leading to similar reconstruction errors for different values of k.
After performing normalization we see that the reconstruction error 
decreases with the value of k, also the value of error is reduced by 
many folds because of normalization
