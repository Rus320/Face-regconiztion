# Face-regconiztion
This project about using SVM model to regconiztion and classify the human face. The dataset used in this example is a preprocessed excerpt of the “Labeled Faces in the Wild”, aka LFW.
which consists of several thousand collated photos of various public figures. A fetcher for the dataset is built into Scikit-Learn.

For a real-world facial recognition task, in which the photos do not come pre-cropped into nice grids, the only difference in the facial classification scheme is the feature selection: you would need to use a more sophisticated algorithm to find the faces, and extract features that are independent of the pixellation. For this kind of application, one good option is to make use of OpenCV, which, among other things, includes pretrained implementations of state-of-the-art feature extraction tools for images in general and faces in particular.

# Summary:
This has been a brief intuitive introduction to the principles behind support vector machines. These models are a powerful classification method, for a number of reasons:

Their dependence on relatively few support vectors means that they are compact and take up very little memory.
Once the model is trained, the prediction phase is very fast.
Because they are affected only by points near the margin, they work well with high-dimensional data—even data with more dimensions than samples, which is challenging for other algorithms.
Their integration with kernel methods makes them very versatile, able to adapt to many types of data.
However, SVMs have several disadvantages as well:

The scaling with the number of samples  N  is  O[N3]  at worst, or  O[N2]  for efficient implementations. For large numbers of training samples, this computational cost can be prohibitive.
The results are strongly dependent on a suitable choice for the softening parameter C. This must be carefully chosen via cross-validation, which can be expensive as datasets grow in size.
The results do not have a direct probabilistic interpretation. This can be estimated via an internal cross-validation (see the probability parameter of SVC), but this extra estimation is costly.
With those traits in mind, I generally only turn to SVMs once other simpler, faster, and less tuning-intensive methods have been shown to be insufficient for my needs. Nevertheless, if you have the CPU cycles to commit to training and cross-validating an SVM on your data, the method can lead to excellent results.

