# FindFace
FindFace is an OpenCV based Python3 program which uses the Viola-Jones algorithm which was proposed by Paul Viola and Michael Jones. The aforementioned algorithm is based on machine learning. The first step involves training a cascade function with a large amount of negative and positive labeled images. Once the classifier is trained, identifying features, namely “HAAR Features,” are extracted from these training images. HAAR features are essentially rectangular features with regions of bright and dark pixels. \
Each feature's value is calculated as a difference between the sum of pixel intensity under the bright region and the pixel intensity under the dark region. All the possible sizes and location of the image is used to calculate these features. An image might contain many irrelevant features and few relevant features which can be used to identify the object. The classifier is trained with the pre-labeled dataset to extract the useful features to get the minimum errors by applying appropriate weights to each feature. An individual feature is called a weak feature. The final classifier is the weighted sum of the weak features. A large region of the image contains the background; only a certain region contains the object to be detected. To increase the detection speed, cascading of classifiers is implemented. In this process, if a region of an image gives even a single negative feature, that region is disregarded for further processing, and the algorithm moves on to the next region. The only region which contains all the identifying features is outlined as the required object in the image. \
