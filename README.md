✈️✈️✈️ Aerial Reconnaissence Multi-class Military Aircraft Recognition (Drone Footage)
This notebook builds an end-to-end multi-class image classifier using TensorFlow 2 Object Detection API to train an SSD-MobileNet model or EfficientDet model with a custom dataset and convert it to TensorFlow Lite format.

Proceedure Roadmap: When multiple annotated subjects in a single image, I am dealing with a multi-object detection problem. Here's a general approach to prepare the dataset for train split testing:

Annotation: Each individual object in an image should be labeled separately. You'll want to create "bounding boxes" around each object in an image, and then label that box with the type of aircraft it contains. Tools like Labelbox, LabelImg, or VGG Image Annotator (VIA) can help with this process.

Format the Data: Your labels should include not only the type of aircraft, but also the location of the bounding box within the image. These labels are usually saved in a structured format such as XML or JSON. For example, in TensorFlow's Object Detection API, they use the TFRecord format.

Model Selection: You'll want to choose a model architecture that's designed for object detection. Some examples include Single Shot MultiBox Detector (SSD), Region-CNN (R-CNN), and You Only Look Once (YOLO).

Training: When you train your model, it will learn to not only classify different types of aircraft but also to predict the bounding boxes around them in the image.

Evaluation: Finally, you'll want to choose an appropriate evaluation metric. For multi-object detection tasks, mean Average Precision (mAP) is often used.
