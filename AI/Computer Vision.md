<p align='right'><a align="right" href="https://github.com/KIRANKUMAR7296/Library/blob/main/Interview.md">Back to Questions</a></p>

# Computer Vision

- How computers see and gain **high level understanding** from `digital images` or `videos`
- Works on **pattern recognition** and **pattern recognition**
- Understand and `automate` the task of human visual system.
- Detecting an `Image` | `Object`, Labeling them has surpassed humans.
- `Faster` than human reaction and `99%` accuracy.
- High amount of Visual Data ( `Images` and `Videos` ) with high processing capabilities.

### How computer sees an image ?
- `0's` and `1's`
- Pixels are **basic fundamental unit** of image.
- Multiple pixels arranged in `matrix` ( `Rows` and `Columns` ) forms an **image**.
- Each pixels have `3 Channels` ( R [255,0,0] | G [0,255,0] | B [0,0,255] ) 8 Bits each.
- Number between `0` to `255` repre`sents `Intensity` of Color.
- Binary : 0 or 1 ( 1 **Bit** )
- Black and White ( `Single` Channel | 8 Bits )
- Grayscale ( `Single` Channel | 8 Bits )
- RGB Color Image ( `3` Channels | `24` Bits | 8 Bits each Channel )

### Image Processing

- Processing `Raw` Images and Applying **Transformation**.
- **Extract Infromation** from Image | Detailed Image Analysis.
- **Enhance** | **Improve** the Image | Change `Color`, `Clearity`, `Size` of Image, `Noise` Reduction, `Contrast`, `Rotation`.
- Prepare Image as an `Input` for a Specific Task.
- Images are converted `to` and `from` **NumPy** Array

> `Black` / `White` and `Greyscale` Images are **Different**
- `Black` and `White` is only Composed with either `Black` ( 000 ) or `White` ( fff )
- `Grayscale` is combination of different `Shades` of `Black` and `White`.
- **Binary** need `1 Bit Per Pixel` for Storage and **Black** and **White** needs `8 Bits Per Pixel` for **Storage**.
- `Black` and `White` will be **Dense** and shall render **Better Quality**.

### Machine Vision

- Image based **Automatic Inspection**, **Object + Pattern Recognition** and **Electromic Component Analysis** ( Industrial Applications ) 
- Capability of Computer to `Perceive` Environment by using Multiple Digital Cameras + Sensors from  Different Locations.
- Cameras with Advance Capability to Electromagnetic Wavelengths + Infrared + Ultraviolet or X Ray.

### Applications 
1. `Autonomous` 🚗 🚙 Self Driving Cars ( Detect Objects and Humans infront of Car, Reverse Parking )
2. Facial Recognition 👦🏻🧒🏻 ( Attendance, FB Friend Recognition )
3. Augmented Reality and Virtual Reality 
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
