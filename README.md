# Computer-Vision
We have classified satellite image data from Hurricane Iota to make a building damage detection model and tested our 4 different kinds of models with both balanced and unbalanced sets.
INFERENCES
For the balanced dataset, Inception has been the best performing model, followed
by ResNet and VGGNetwhile our custom model somewhat performed poorly. For
the custom model, 65 damaged buildings were reported undamaged, for VGGNet,
ResNet and Inception, these values are 108, 20 and 30 which is less with respect to
total 2000 buildings. This means, damaged buildings will be more accurately spotted.
And, while the three transfer learning models labelled 15, 28 and 13 number of
undamaged buildings as damaged, our custom model classified 935 undamaged
buildings as damaged. This means the custom model, will get emergency managers
to give assistance to those house which is not even damaged (that too in higher
numbers). But this can be tolerated to some extent. Overall performance of transfer
learning models have been better with respect to the custom model on the balanced
dataset.
For the unbalanced dataset, scenario is kind of reversed. Custom model became the
model with overall better performance on different metrics of evaluation,
performances of ResNet and Inception models have been terribly worse. VGGNetis
still performing good and is comparable to the performance of the custom model.
But with respect to safety in real world, custom model seemed to perform best as it
classify among others less number of damaged buildings as undamaged. Other
models report very high number of damaged buildings as undamaged which is not a
good sign.
Final conclusion from the model performances would be that such models are
deployable only if some other methods are also used along with this. Model
accuracies need to be improved by either training it on more dataset or taking
models pretrained on satellite images.
FUTURE WORKS
Use of Hurricane delta: This dataset as instructed, contains large scale images of
whole hurricane damaged area. From these large scale images, localities with
buildings can be extracted as squared size images. These new images can either be
used for more training on our models, or can be used to see what our models
predict. Due to time constraint and lack of relevant knowledge, we decided to drop
this idea for now and add it to our future works.
Transfer learning models pretrained on geospatial image datasets: Models were
trained on 'Imagenet', but we did classification of satellite images which is not much
close to the Imagenet dataset, even though the performance was good. Those
models which have been pretrained on datasets like 'BigEarthNet'
(https://bigearth.net/) will be best suited for classification in this case using transfer
learning. We tried downloading model weights from https://git.tuberlin.de/rsim/BigEarthNet-MM_19-classes_models and assigning it to our model,
but due to version differences it didn't worked out this time. Performance of such
model will no doubt be the best of all which we will address in our future work on
this project.
