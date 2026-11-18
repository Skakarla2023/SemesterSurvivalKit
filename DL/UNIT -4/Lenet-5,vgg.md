# **LeNet-5 and VGG in Deep Learning**

LeNet-5 and VGG are two popular **Convolutional Neural Network (CNN) architectures** used for image recognition and classification.

Both architectures use convolutional layers, pooling layers and fully connected layers to identify objects in images.

Let's understand them one by one.

# **1. LeNet-5 Architecture**

## **What is LeNet-5?**

**LeNet-5** is one of the earliest CNN architectures, developed by Yann LeCun and his team.

- It was mainly designed for handwritten digit recognition.
- It is used to recognize numbers from 0 to 9.
- It uses convolution, pooling and fully connected layers.
- It has 7 trainable layers (excluding the input layer).

**Example:** When we give a handwritten digit image (like 5), LeNet-5 identifies it as the number 5.

## **Architecture of LeNet-5**

[Convolutional Neural Networks: 1998-2023 Overview | SuperAnnotate](https://images.openai.com/static-rsc-4/quHKU_YYocbXTkYEExfCNckQVB54hSw_NdO44hz98F8bVRa0hCRh31Oci1jOWbc_F2nqcriV-EfxIkUKPGyfOv1hCDySqQaFU4MWymaL8em3mBEPjdaPgRrlnOSk-oaTFIJPlPGj6w0oq16jb0gauez-lthTfQHpUl4hL3q7IrQ?purpose=inline)

[superannotate.com](https://www.superannotate.com/blog/guide-to-convolutional-neural-networks?utm_source=chatgpt.com)

### **Layers of LeNet-5**

LeNet-5 contains the following layers:

**1. Input Layer**

- Takes a handwritten digit image as input.
- The original LeNet-5 uses a 32 × 32 grayscale image.
- Grayscale means the image contains only one channel.

**2. C1 – Convolutional Layer**

- Contains 6 filters of size 5 × 5.
- Extracts simple features like edges and lines.
- Produces 6 feature maps of size 28 × 28.

**3. S2 – Subsampling Layer (Pooling)**

- Reduces the size of feature maps.
- Uses 2 × 2 average pooling with stride 2.
- Produces feature maps of size 14 × 14.
- Reduces computation.

**4. C3 – Convolutional Layer**

- Contains 16 feature maps.
- Extracts more complex features by combining previously detected patterns.
- Produces feature maps of size 10 × 10.
- In the original LeNet-5, this layer uses a partial connection scheme rather than connecting every input map to every output map.

**5. S4 – Subsampling Layer**

- Uses average pooling.
- Reduces the feature map size from 10 × 10 to 5 × 5.
- Helps reduce the amount of data.

**6. C5 – Convolutional Layer**

- Contains 120 filters of size 5 × 5.
- Extracts high-level features.
- Produces 120 outputs of size 1 × 1.

**7. F6 – Fully Connected Layer**

- Contains 84 neurons.
- Combines the extracted features.
- Helps identify the digit.

**8. Output Layer**

- Contains 10 outputs.
- Each output represents one digit from 0 to 9.
- Identifies the most likely digit.

### **Simple flow of LeNet-5**

**Input Image**

32 × 32 × 1

**C1 – Convolution**

6 feature maps (28 × 28)

**S2 – Average Pooling**

6 feature maps (14 × 14)

**C3 – Convolution**

16 feature maps (10 × 10)

**S4 – Average Pooling**

16 feature maps (5 × 5)

**C5 – Convolution**

120 outputs

**F6 – Fully Connected**

84 neurons

**Output Layer**

10 classes (0–9)

## **Important Features of LeNet-5**

- Uses convolutional and subsampling layers.
- Uses 5 × 5 convolution filters.
- Uses average pooling.
- Designed mainly for handwritten digit recognition.
- Has a relatively simple architecture compared to modern CNNs.

## **Advantages of LeNet-5**

1. Simple architecture and easy to understand.
2. Requires less computational power.
3. Performs well on handwritten digit recognition.
4. Introduced important concepts used in modern CNN architectures.

## **Disadvantages of LeNet-5**

1. Not suitable for very complex images.
2. Has limited feature extraction capability compared to deeper CNNs.
3. Designed mainly for small grayscale images.

# **2. VGG Architecture**

## **What is VGG?**

**VGG (Visual Geometry Group)** is a deep CNN architecture developed by researchers at the University of Oxford.

It was introduced in 2014.

- It is mainly used for image classification.
- It uses small 3 × 3 convolution filters.
- It has a deep network with multiple convolutional layers.
- It learns simple features first and gradually learns complex features.

VGG has different versions, such as:

- VGG-16
- VGG-19

The numbers 16 and 19 represent the number of weight layers (convolutional + fully connected layers).

## **Main Idea of VGG**

VGG uses multiple small 3 × 3 filters instead of using large filters.

**Why does VGG use 3 × 3 filters?**

- Small filters capture simple features like edges and patterns.
- Multiple convolution layers help learn complex features.
- It introduces more non-linearity through multiple ReLU activations.

For example:

- First layers detect edges.
- Middle layers detect shapes and textures.
- Deeper layers detect objects like faces, cars and animals.

## **Architecture of VGG-16**

[An overview of VGG16 and NiN models | by Khuyen Le | Medium](https://images.openai.com/static-rsc-4/9B0VKlVzO3P-RlenEzv2AZIu5ZHdx-xg_jeSav7dbfVUA5PLxmsWoGcfPPMLMuX5hDjioZgywtK9Egjav9cgVLC299y22VbsBzazPVCnv3NmGn90dfy6LoJFRyUHAMRMmQXM6HTHiAUe18TnNpjI3JrfBpyZ35vo9RKLnE3BnyE?purpose=inline)

[lekhuyen.medium.com](https://lekhuyen.medium.com/an-overview-of-vgg16-and-nin-models-96e4bf398484?utm_source=chatgpt.com)

VGG-16 takes an image of size 224 × 224 × 3 as input.

It consists of 5 convolution blocks followed by 3 fully connected layers.

### **Layers of VGG-16**

**1. Input Layer**

- Takes a colored image as input.
- Image size is 224 × 224 × 3.
- Three channels represent RGB (Red, Green and Blue).

**2. Block 1**

- Contains 2 convolutional layers.
- Each layer uses 64 filters of size 3 × 3.
- Uses ReLU activation.
- Followed by 2 × 2 max pooling.

**3. Block 2**

- Contains 2 convolutional layers.
- Each layer uses 128 filters of size 3 × 3.
- Extracts more complex features.
- Followed by max pooling.

**4. Block 3**

- Contains 3 convolutional layers.
- Each layer uses 256 filters of size 3 × 3.
- Detects more detailed patterns and shapes.
- Followed by max pooling.

**5. Block 4**

- Contains 3 convolutional layers.
- Each layer uses 512 filters of size 3 × 3.
- Extracts more complex features.
- Followed by max pooling.

**6. Block 5**

- Contains 3 convolutional layers.
- Each layer uses 512 filters of size 3 × 3.
- Detects high-level features.
- Followed by max pooling.

**7. Fully Connected Layers**

- Contains 3 fully connected layers.
- First layer has 4096 neurons.
- Second layer has 4096 neurons.
- Final layer has 1000 neurons for 1000 image classes in the original ImageNet model.

**8. Output Layer**

- Uses Softmax to produce class probabilities.
- Predicts the image category.

### **Simple flow of VGG-16**

**Input Image**

224 × 224 × 3

**Block 1**

2 Conv layers – 64 filters

**Block 2**

2 Conv layers – 128 filters

**Block 3**

3 Conv layers – 256 filters

**Block 4**

3 Conv layers – 512 filters

**Block 5**

3 Conv layers – 512 filters

**3 Fully Connected Layers**

4096 → 4096 → 1000

**Output Layer**

Image Classification

Each convolution block ends with 2 × 2 max pooling.

## **Important Features of VGG**

1. Uses small 3 × 3 convolution filters.
2. Has a deep architecture.
3. Uses ReLU activation.
4. Uses max pooling to reduce image dimensions.
5. Learns simple features in the initial layers and complex features in deeper layers.
6. VGG-16 has 16 weight layers, while VGG-19 has 19 weight layers.

## **Advantages of VGG**

1. Simple and uniform architecture.
2. Extracts complex image features effectively.
3. Provides good image classification performance.
4. Can be used for transfer learning.

**Transfer Learning:** Using a model already trained on a large dataset for a new, related task.

## **Disadvantages of VGG**

1. Requires high computational power.
2. Has a large number of parameters.
3. Requires more memory.
4. Training takes more time.

# **3. Difference Between LeNet-5 and VGG**

| Feature                | LeNet-5                       | VGG-16               |
| ---------------------- | ----------------------------- | -------------------- |
| Developed by           | Yann LeCun and team           | Oxford researchers   |
| Introduced             | 1998                          | 2014                 |
| Architecture           | Simple and shallow            | Deep                 |
| Input image            | 32 × 32 grayscale             | 224 × 224 RGB        |
| Filter size            | 5 × 5                         | 3 × 3                |
| Pooling                | Average pooling               | Max pooling          |
| Main use               | Handwritten digit recognition | Image classification |
| Complexity             | Low                           | High                 |
| Fully connected layers | 2                             | 3                    |

## **4. Quick Revision – Important Terms**

| Term                  | Meaning                                        |
| --------------------- | ---------------------------------------------- |
| LeNet-5               | Early CNN architecture for digit recognition   |
| VGG                   | Deep CNN architecture for image classification |
| Convolution           | Extracts image features                        |
| Filter / Kernel       | Detects patterns in an image                   |
| Feature Map           | Output after convolution                       |
| Average Pooling       | Takes the average value                        |
| Max Pooling           | Takes the maximum value                        |
| ReLU                  | Removes negative values                        |
| Fully Connected Layer | Combines features for classification           |
| Transfer Learning     | Reuses a pretrained model for a new task       |

## **Remember these exam points**

**LeNet-5:**

- Developed by Yann LeCun and team.
- Designed for handwritten digit recognition.
- Uses 5 × 5 filters.
- Uses average pooling.
- Has 7 trainable layers.

**VGG-16:**

- Developed by Oxford researchers.
- Uses 3 × 3 filters.
- Has 5 convolution blocks.
- Uses max pooling.
- Has 16 weight layers.
- Uses 3 fully connected layers.

**Easy way to remember:**

- **LeNet-5 =** Simple CNN + Handwritten digits.
- **VGG =** Deep CNN + Small 3 × 3 filters + Image classification.

For your exam, focus especially on the architecture diagrams, layer-by-layer working, important filter sizes and the difference between LeNet-5 and VGG.
