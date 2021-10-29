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
2. `Facial recognition` 👦🏻🧒🏻 ( Attendance, FB friend recognition )
3. `AR` : Augmented Reality and `VR` : Virtual Reality 
4. Health care ( `XRay` and `MRI Scan` ) 👨🏻‍⚕️💉🩺
5. Video motion analysis ( Detect faces and objects in videos )
6. Image segmentation ( Camera detects the multiple faces in a group selfie )
7. Scene reconstruction ( 3D model creation in architecture )
8. Image restoration ( Filtering blur images and removing noise )
9. Search by image [`Image.Google`](https://images.google.com/) 🖼
10. `Robotics` 🤖

### Important terms

### 1. Pixel Manipulation
- Converting image from one form to another ( e.g. `BGR` to `HSV` or `Grayscale` )

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

1. `Retail`
- Store cameras to understand customer `behaviour`, `gender` and `age`
- Help shops to store products ( Item placement ) on the basis of **customer shopping experience**.
- `Anti theft` : Face recognition, spying and detecting ( Hiding product in bag )
- `Inventory management` : Accurate estimate of the items available in the store, analyze increase in demand.

2. `Manufacturing`
- Maintenance with the help of robots, sensors and cameras.
- Packing, unpacking and assembly of car.

3. `Healtcare`
- Medical image analysis ( `MRI`, `CT Scan`, `XRay` ) detect and diagnost anomalies, cancer and tumors. 

4. `Autonomous` ( Self driving car )
- Object detection in image and video.
- Distinguish traffic lights, vehicles, persons etc.

5. `Insurance` 
- Avoiding accidents and collisions, integrated in industrial machinery, cars and drones.
- Image analysis and estimate repair cost.

6. `Agriculture`
- Grain production, pesting, early diagnosis helps farmer to make appropriate measures.
- Robots monitor entire farm, need of water, spray herbicides and helps production cost.
- Sorting fruits, vegetables and even flowers.
- Identify shape, size, color, weight and texture.

7. `Defense` and `Security`
- High security requirements in retail, companies, banks, malls, shopping centre, etc.
- Cargo inspection on ports, surveillance of sensitive places such as embassy, power plants, hospitals, railroads and stadiums.
- Spy on enemy terrain, automatic identification of anomalous behavior, search and rescue operations.

### Typical task in computer 

1. `Image Classification`
- Tourist attractions based on location image.
- Type of vehicle ( Mini, Hatchback, Sedan, SUV, MPV )

2. `Localization`
- Find the location of a single object in an image.
- Bounding box around image, automatic cropping.

3. `Object Detection`
- Detect multiple objects in a single image or video.
- Fast detection as compared to human eye.
- Detect and count total males and females in images.
- Finding object in the image and difference between two images.

4. `Object Tracking`
- Motion image object detection ( Capture consecutive video frames )
- Motion sensor cameras to capture ( Name plates ) speeding vehicles on expressways.
- `Robot` goal keepers and constant football, basketball and cricket monitoring.

### Business Use Cases

1. `Visual Search Engines`
- `Google Image`, `Bing` and `Yahoo Image Search`
- `Google Lens` ( Detailed Information from the Image
- `Pinterest Lens` ( Visual Search for Online Shopping )

2. Face recognition at `Facebook`
- Detect face and recognize the person in an image + auto tagging.
- Recognize facial expression.

3. `Amazon Go` stores
- Shopping without `queue`, easy `scan` and `pay` ( QR Code )
- Motion and weight sensors, cameras and real time product price calculation.

4. `Tesla` Auto Pilot
- `Autonomous` driving ( Eight panaromic cameras give `360` degree visibility upto `250` meters range )
- `Ultrasonic sensors` are installed to detect objects, traffics and environment.
- `Radar` sensors to process information about surroundings.
- Adjust speeds depending on traffic conditions, brakes when approaching obstacles, change of lane and parking.

5. `Microsoft` Inner Eye
- Assist `radiology` and `surgeons` who have to works closely for inner body parts.
- The technology presents `3D models` of tumors ( Measure and track size and spread ) 

### Deep Learning ( Convolutional Neural Network CNN )

1. Create a dataset comprised of annotated image or use existing one ( Annotation can be classes or bounding box )
2. Extract feature from the image ( Face, car, animal, object, person, etc. )
3. Train a model based on features.
4. Evaluate the model with new unseen images.

But it is very `costly` if we follow a `supervised approach`

### Existing Data Sets

1. `ImageNet` : `14 million` images annotated with `WordNet` ( `1M` images contains bounding box )
2. Microsoft `COCO` ( Common Object Context ) : `32,8000` ( `2.5M` labelled Instances )
3. `CelebFaces` attributes dataset ( `CelebA` ) : `200K` celebrity images.
4. `Indoor` scene recognition : `15,620` images of indoor objects. 
5. `Plant` image analysis : `1M` images of plants from `11 different species`

### `HAAR` ( First real time face detector )
- Digital image `feature` used in `object` recognition.
- Features represents `edges` and `lines`
- In case of face features allow for capturing important elements ( Nose, mouth, eyes and distance between eye brows )
