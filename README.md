# Handwritten-SVM
Handwritten Digits Reorganization Using SVM. 
##Problem Understanding####
The images are flattend into csv and one row represent one image.
we have to classify images which is a multiclass problem.
we have to use svm techniques and best kernel for this problem.
Comparison for all the kernels is to be provided


###Note:
i havent scaled the data set as all columns varies from range 0-255.No Particular column is driving the output.
i havent removed all zeros columns as If in test data digit is not in center then it might then that column might be zero for training but it might be non-zero in test.
mnist data is clean and it has no left and right shifts or rotation
But taking care of all these i haven't removed columns with all zeros values in train and test


Only used 10% of training data for this work.
## used doParallel library for fast computation using multi cores


Used linear,poly and Radial and 5-fold cv for cross validation.


linear kernel was giving 91% accuracy on test set which is good.
poly kernel was giving 95.04% accuracy which degree-2 so adding slightly non-linearity 
accuracy improves significantly for same C value justified by Cross-validation.
radial kernel is having very less sigma value employing that and C=1 employing that not much amount of non-linearity in
this model and accuracy also is 95.05% almost same as degree-2 poly kernel.
So, on whole data is having some amount of non-linearity but not so much non-linearity and Poly(degree-2) model being 
having optimal bias and variance as its bias is less  than linear(accuracy) and variance(less complex) is less than radial kernel
with same amount of accuracy.


