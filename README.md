# Differential privacy in Image captioning

Modern machine learning is increasingly applied to create amazing new technologies and user experiences, many of which involve training machines to learn responsibly from sensitive data, such as personal photos or email. Ideally, the parameters of trained machine-learning models should encode general patterns rather than facts about specific training examples. To ensure this, and to give strong privacy guarantees when the training data is sensitive, it is possible to use techniques based on the theory of differential privacy. In particular, when training on users’ data, those techniques offer strong mathematical guarantees that models do not learn or remember the details about any specific user. Especially for deep learning, the additional guarantees can usefully strengthen the protections offered by other privacy techniques, whether established ones, such as thresholding and data elision, or new ones, like TensorFlow Federated learning.

## Dataset
The dataset used in this project is the MS COCO dataset for image captioning which can be found [here](https://www.tensorflow.org/datasets/catalog/coco).

## Approach
Image captioning has been a key components of image search engines and the discovery of new and more accurate sequence2sequence models such as encoder-decoder architectures and transformers has led to an increase in highly efficient image captioning models and image search engines. 
Since we have achieved great heights in successfully performing sequential tasks using deep learning, the task that comes to mind is how to make our models more secure and differentially private. Tensorflow came up with a library known as Tensorflow-privacy in March, 2019, which attracted more researchers and developers towards this field.
The project aims at introducing differential privacy to an image captioning model by adding noise to the optimization process. This leads to an increase in loss, which is an expected result.
This loss is denoted by *ε*(epsilon) and is known as privacy loss. 
Our aim is to reduce *ε* as much as possible.
For further details, read the tensorflow blog [here](https://blog.tensorflow.org/2019/03/introducing-tensorflow-privacy-learning.html).

## Results:
We have been able to achieve a privacy loss of 0.61. 
Please use the checkpoints provided to load the weights of the model.

## References
We have taken the code from tensorflow-privacy tutorial notebook, but instead of using the tensorflow-privacy library we've designed our custom class for creating differential private optimizers.

