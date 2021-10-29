<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Computer Vision

- How computers gain **high level understanding** from a `digital image` or `video`
- Works on `pattern recognition`
- Understand and `automate` the task of human visual system.
- Detecting an `image` or `object`, labeling them has surpassed humans.
- `Faster` than human reaction with `99%` accuracy.
- High amount of visual data, i.e. `images` and `videos` with high processing capabilities.

### How computer sees an image ?
- `0's` and `1's`
- `Pixel` is a **basic fundamental unit** of an image.
- Multiple pixels arranged in `matrix`, i.e. `rows` and `columns` forms an **image**.
- Each pixels have `3 Channels` | `R[255,0,0]`, `G[0,255,0]`, `B[0,0,255]` | `8 bits` each.
- Number between `0` to `255` represents `intensity` of color.

### `Types` of Images 

- `Binary` : `0` or `1` | `1 bit`
- `Black` n `white` : `Single` channel | `8 bits`
- `Grayscale` : `Single` channel | `8 bits`
- `RGB` color image : `3` channels | `24 bits` | `8 bits` each channel.
- `Black` n `White` and `greyscale` images are `different`
- `Black` n `white` is only composed with completely either black : `000` or white : `fff`
- `Grayscale` is combination of different `shades` of `black` and `white`
- **Binary** need `1 bit per pixel` for storage and **black** n **white** needs `8 bits per pixel` for **storage**.
- `Black` n `white` will be **dense** and shall render **better quality**.

### Image Processing

- `Processing` raw images and applying `transformation`
- `Extract` infromation from image | Detailed image analysis.
- `Enhance` : **Improve** the image quality and appearance. 
- Change `color`, `clarity`, `size` of image, `noise` reduction, `contrast`, `rotation`
- Prepare image as an `input` for a specific task.
- Images are converted to and from `NumPy array`

### Machine Vision

- Image based **automatic inspection** (Airports and malls entry gate)
- **Object + pattern recognition**. 
- **Electromic Component Analysis** ( Industrial Applications ) 
- Capability of computer to `perceive` environment by using multiple digital cameras + sensors from multiple locations.
- Cameras with advance capturing capabilities : Electromagnetic Wavelengths + Infrared + Ultraviolet or X Ray.

### Applications 
1. `Autonomous` 🚗 🚙 self driving cars ( Detect objects and humans infront of car, reverse parking )
2. `Facial recognition` 👦🏻🧒🏻 ( Attendance, FB Friend Recognition )
3. `AR` : Augmented Reality and `VR` : Virtual Reality 
4. Health Care ( X Ray and MRI Scan ) 👨🏻‍⚕️💉🩺
5. Video Motion Analysis ( Detect Face, Object in Video )
6. Image Segmentation ( Camera Detects the Multiple Faces in a Group Selfie )
7. Scene Reconstruction ( 3D Model Creation in Architecture )
8. Image Restoration ( Filtering Blur Images and Removing Noise )
9. Search By Image [`Image.Google`](https://images.google.com/) 🖼
10. Robotics 🤖

### Important Terms

### 1. Pixel Manipulation
- Converting Image from one form to another ( e.g. BGR to HSV or Grayscale )

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
    <td>Turn Black Pixels into White Pixels</td>
    <td>Turn White Pixels into Black Pixels</td>
  </tr>
</table>

<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>


### Industry Applications

1. Retail
- Store Cameras to Understand Customer `Behaviour`, `Gender` and `Age`.
- Help Shops to Store Products ( Item Placement ) on the basis of **Customer Shopping Experience**.
- **Anti Theft** : Face Recognition and Spying and Detecting Hiding Product in Bag.
- **Inventory Management** : Accurate Estimate of the Items Available in the Store, Analyze Increase in Demand.

2. Manufacturing 
- Maintenance with the Help of Robots, Sensors and Cameras.
- Packing, Unpacking and Assembly of Car.

3. Healtcare
- Medical Image Analysis ( MRI, CT Scans, X Rays ) Detect and Diagnost Anomalies, Cancer and Tumors. 

4. Autonomous ( Self Driving Car )
- Object Detection in Image and Video.
- Distinguish Traffic Light, Vehicles, Person etc.

5. Insurance 
- Avoiding Accidents and Collisions, Integrated in Industrial Machinery, Cars and Drones.
- Image Analysis and Estimate Repair `Cost`.

6. Agriculture
- Grain Production, Pesting, Early Diagnosis helps Farmer to make appropriate Measures.
- Robots monitor Entire Farm, Need of Water, Spray Herbicides and Helps Production Cost.
- Sorting Fruits, Vegetables and even Flowers.
- Identify Shape, Size, Color, Weight and Texture.

7. Defense and Security
- High Security Requirements in Retail, Companies, Banks, Malls, Shopping Centre etc Analyze Image from Security Cameras.
- Cargo Inspection on Ports, Surveillance of Sensitive Places such as Embassy, Power Plants, Hospitals, Railroads and Stadiums.
- Spy on Enemy Terrain, Automatic Identification of Anomalous Behavior, Search and Rescue Operations.

### Typical Task in Computer 

1. Image Classification
- Tourist Attractions based on Location Image
- Type of Vehicle ( Mini, Hatchback, Sedan, SUV, MPV )

2. Localization
- Find the Location of a Single Object in an Image.
- Bounding Box around Image, Automatic Cropping

3. Object Detection
- Detect Multiple Objects in a Single Image or Videos.
- Fast Detection as Compared to Human Eye.
- Detect and Count Total Males and Females in Images.
- Finding Object in the Image and Difference between the Image.

4. Object Tracking
- Motion Image Object Detection ( Capture Consecutive Video Frames )
- Motion Sensor Cameras to Capture ( Name Plates ) Speeding Vehicles on Expressway
- Robot Goal Keepers and Constant Football, Basketball and Cricket Monitoring.

### Business Use Cases

1. Visual Search Engines
- Google Image, Bing and Yahoo Image Search
- Google Lens ( Detailed Information from the Image
- Pinterest Lens ( Visual Search for Online Shopping )

2. Face Recognition at Facebook
- Detect Face and Recognize the Person in an Image or Video.
- Resognize Facial Expression.

3. Amazon Go Stores
- Shopping without Queue, Scan and Pay ( QR Code )
- Motion and Weight Sensors, Cameras and Real Time Product Price Calculation.

4. Tesla Auto Pilot
- Autonomous Driving ( Eight Panaromic Cameras give 360 Degree Visibility upto 250 meters Range )
- Ultrasonic Sensors are Installed to Detect Objects.
- Radar Sensors to Process Information about Surroundings.
- Adjust Speeds depending on Traffic Conditions, Brakes when approaching Obstacles, Change of Lane and Parking.

5. Microsoft Inner Eye
- Assist Radiology and Sergons who have to Works Closely for Inner Body Parts.
- The Technology Presents 3D Models of Tumors ( Measure and Track Size and Spread ) 
### Deep Learning ( Convolutional Neural Network CNN )

1. Create a Data Set comprised of Annotated Image or Use Existing One ( Annotation can be Category, Bounding Box and Classes )
2. Extract Feature from the Image ( Face, Car, Animal, Object )
3. Train a Model based on Features.
4. Evaluate the Model with New Unseen Image.

But It is very Costly if we follow a Supervised Approach

### Existing Data Sets

1. `ImageNet` : `14` Million Images Annotated with WordNet ( `1` Million Images contain Bounding Box )
2. Microsoft `COCO` ( Common Object Context ) : `32,8000` ( `2.5` Million Labelled Instances )
3. CelebFaces Attributes Dataset ( `CelebA` ) : `200K` Celebrity Images.
4. `Indoor` Scene Recognition : `15,620` Images of Indoor Objects 
5. `Plant` Image Analysis : `1` Million Images of Plants from 11 Different Species.

### HAAR ( First Real Time Face Detector )
- Digital Image `Feature` used in Object Recognition.
- Features represents Edges and Lines.
- In Case of Face these Features allow for Capturing Important Elements ( Nouse, Mouth, Eyes and Distance between Eye Brows )
