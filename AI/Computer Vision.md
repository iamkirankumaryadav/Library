<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Computer Vision
- Think of computer vision as teaching a computer to "see" and understand the world like a human does.
- It's a field of AI that enables computers to interpret and understand visual information from the world, such as images and videos.

### Simple Example: Facial Recognition
- One of the most common applications of computer vision is facial recognition. Let's break down how it works:

1. **Image Capture:** A camera takes a picture of a person's face.
2. **Feature Extraction:** The computer analyzes the image, looking for specific features like the distance between the eyes, the shape of the nose, and the contour of the lips.
3. **Comparison:** The extracted features are compared to a database of known faces.
4. **Identification:** If a match is found, the computer identifies the person in the image.

### Real-world Applications
- **Security:** Facial recognition is used in airports and other secure locations for identification and access control.
- **Social Media:** Apps like Facebook use facial recognition to suggest tagging friends in photos.
- **Self-driving Cars:** Cars use computer vision to detect pedestrians, other vehicles, and traffic signs.
- **Medical Imaging:** Doctors use computer vision to analyze X-rays, MRIs, and other medical images to detect abnormalities.
- Detecting an image or object and labelling them has surpassed humans. Faster than human reaction with 99% accuracy.
- High amount of visual data, i.e. images and videos with high processing capabilities.

### How computer see an image?
- 0's and 1's. Pixel is a **basic fundamental unit** of an image.
- Multiple pixels arranged in a matrix, i.e. rows and columns form an **image**.
- Each pixels have 3 Channels | B[255,0,0], G[0,255,0], R[0,0,255] | 8 bits each.
- Normally the order is RGB channel but OpenCV reads the image channel in order BGR.
- The number between 0 to 255 represents the intensity of colour.

### Types of Images
- Binary: 0 or 1 | 1 bit
- Black and white: Single channel | 8 bits
- Grayscale: Single channel | 8 bits
- RGB colour image: 3 channels | 24 bits (8 bits each channel)
- Black/White and greyscale images are different.
- Black/White is only composed with completely either black: 000 or white: fff.
- Grayscale is a combination of different shades of black and white.
- **Binary** need 1 bit per pixel for storage and **black** n **white** needs 8 bits per pixel for **storage**.
- Black/White will be **dense** and shall render **better quality**.

### Image Acquisition
- Techniques for capturing images using various devices like cameras, scanners, and medical imaging equipment.

### Image Processing
- **Image Filtering:** Applying filters to enhance or reduce the noise in images.
- **Image Transformation:** Manipulating images through geometric transformations.
- **Image Extraction:** Extract information from the image (Detailed image analysis)
- **Image Enhancement:** Techniques to improve the image quality and appearance. 
- Colour, clarity, size, noise reduction, contrast, rotation, sharpness, orientation, and scale.
- Prepare an image as an input for a specific task. Images are converted to and from the NumPy array

### Feature Extraction
- **Edge Detection:** Identifying boundaries between regions with different intensity levels.
- **Corner Detection:** Locating points of significant intensity change in an image.
- **Texture Analysis:** Analyzing the spatial arrangement of patterns in an image.
- **Color Analysis:** Extracting information from the colour content of an image.

### Machine Vision
- Image-based **automatic inspection** (Airports and malls entry gate)
- **Object + Pattern Recognition**. 
- **Electronic Component Analysis** (Industrial Applications) 
- Capability of the computer to perceive the environment by using multiple digital cameras + sensors from multiple locations.
- Cameras with advanced capturing capabilities: Electromagnetic Wavelengths + Infrared + Ultraviolet or X-Ray.

### Object Detection and Recognition
- **Object Detection:** Identifying the presence and location of objects in an image.
- **Object Recognition:** Classifying and categorizing detected objects.
- **Object Tracking:** Following the movement of objects over time.

### Image Segmentation
- **Partitioning:** Dividing an image into meaningful regions or segments.
- **Semantic Segmentation:** Assigning semantic labels to each pixel in an image.
- **Instance Segmentation:** Identifying and segmenting individual instances of objects in an image.

### Applications 
1. **Autonomous Self-driving Cars** 🚗🚙 (Detect objects and humans in front of car, reverse parking)
2. **Facial Recognition:** Identifying individuals based on their facial features 👦🏻🧒🏻 (Attendance, FB friend recognition)
3. **AR:** Augmented Reality and **VR:** Virtual Reality 
4. **Medical Image Analysis or Health Care:** Detecting diseases and anomalies in medical images (XRay and MRI Scan) 👨🏻‍⚕️💉🩺
5. **Video Motion Analysis:** (Detect faces and objects in videos)
6. **Security Surveillance:** Monitoring and analyzing video feeds for security purposes.
7. **Image Segmentation** (Camera detects the multiple faces in a group selfie)
8. **Scene Reconstruction** (3D model creation in architecture)
9. **Image Restoration** (Filtering blur images and removing noise)
10. Google, Microsoft, Pinterest, etc. Search by image [`Image.Google`](https://images.google.com/) 🖼
11. **Robotics** 🤖: Guiding robots to perform tasks in the real world.

### Important Terms
### 1. Pixel Manipulation
- Converting image from one form to another.  
- e.g. BGR to HSV or Grayscale

### 2. Pixel Filtering

<table>
  <tr>
    <th>Dilation</th>
    <th>Erosion</th>
  </tr>
  <tr>
    <th>cv2.dilate( )</th>
    <th>cv2.erode( )</th>
  </tr>
  <tr>
    <td>Turn black pixels into white pixels</td>
    <td>Turn white pixels into black pixels</td>
  </tr>
</table>

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>


### Industry Applications

1. Retail
- Store cameras to understand customer behaviour, gender and age.
- Help shops to store products (Item placement) based on **customer shopping experience**.
- Anti-theft: Face recognition, spying and detecting (Hiding product in bag)
- **Inventory Management:** Accurate estimate of the items available in the store, analyze the increase in demand.

2. Manufacturing
- Maintenance with the help of robots, sensors and cameras. Packing, unpacking and assembly of car.

3. Healthcare
- Medical image analysis (MRI, CT Scan, XRay) detect and diagnoses anomalies, cancer and tumours. 

4. Autonomous (Self-driving car)
- Object detection in image and video. Distinguish traffic lights, vehicles, persons etc.

5. Insurance 
- Avoiding accidents and collisions, integrated into industrial machinery, cars and drones.
- Image analysis and estimate repair cost.

6. Agriculture
- Grain production, pesting, and early diagnosis help farmer to take appropriate measures.
- Robots monitor the entire farm, need water, spray herbicides and help production costs.
- Sorting fruits, vegetables and even flowers.
- Identify shape, size, colour, weight and texture.

7. Defense and Security
- High-security requirements in retail, companies, banks, malls, shopping centres, etc.
- Cargo inspection on ports, surveillance of sensitive places such as embassies, power plants, hospitals, railroads and stadiums.
- Spy on enemy terrain, automatic identification of anomalous behaviour, search and rescue operations.

### Typical task in computer 

1. Image Classification
- Tourist attractions based on location image.
- Type of vehicle (Mini, Hatchback, Sedan, SUV, MPV)

2. Localization
- Find the location of a single object in an image.
- Bounding box around the image, automatic cropping.

3. Object Detection
- Detect multiple objects in a single image or video.
- Fast detection as compared to the human eye.
- Detect and count total males and females in images.
- Finding objects in the image and the difference between the two images.

4. Object Tracking
- Motion image object detection (Capture consecutive video frames)
- Motion sensor cameras to capture (Nameplates) speeding vehicles on expressways.
- Robot goalkeepers and constant football, basketball and cricket monitoring.

### Business Use Cases
1. Visual Search Engines
- Google Image, Bing and Yahoo Image Search.
- Google Lens (Detailed Information from the Image)
- Pinterest Lens (Visual Search for Online Shopping)

2. Face recognition on Facebook
- Detect face and recognize the person in an image + auto-tagging.
- Recognize facial expressions.

3. Amazon Go Stores
- Shopping without queue, easy scan and pay (QR Code)
- Motion and weight sensors, cameras and real-time product price calculation.

4. Tesla Auto Pilot
- Autonomous driving (Eight panoramic cameras give 360-degree visibility up to 250 meters range)
- Ultrasonic sensors are installed to detect objects, traffic and environment.
- Radar sensors to process information about surroundings.
- Adjust speeds depending on traffic conditions, brakes when approaching obstacles, change of lane and parking.

5. Microsoft Inner Eye
- Assist radiology and surgeons who have to works closely with inner body parts.
- The technology presents 3D models of tumours (Measure and track size and spread) 

### Deep Learning (Convolutional Neural Network CNN)
1. Create a dataset comprised of annotated images or use existing ones (Annotation can be classes or bounding box)
2. Extract features from the image (Face, car, animal, object, person, etc.)
3. Train a model based on features.
4. Evaluate the model with new unseen images.

But it is very costly if we follow a supervised approach.

### Existing Data Sets
1. ImageNet: 14 million images annotated with **WordNet** (1M images contain bounding box)
2. Microsoft COCO (Common Object Context): 32,8000 (2.5M labelled Instances )
3. CelebFaces attributes dataset (CelebA): 200K celebrity images.
4. Indoor scene recognition: 15,620 images of indoor objects. 
5. Plant image analysis: 1M images of plants from 11 different species.

### HAAR (First real-time face detector )
- Digital image feature used in face recognition.
- Features represent edges and lines.
- Face feature allows for capturing important elements (Nose, mouth, eyes and distance between eyebrows)

### Deep Learning for Computer Vision:
- **Convolutional Neural Networks (CNNs):** A powerful class of neural networks for image analysis and recognition.
- **Transfer Learning:** Leveraging pre-trained models to improve performance on new tasks.
- **Generative Models:** Creating new images or videos from existing data.
