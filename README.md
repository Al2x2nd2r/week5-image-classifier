# week5-image-classifier
# Computer Vision Image Classifier
## Project Overview
This project implements image classification using computer vision concepts from Chapter 24. The AI can recognize objects in images using a neural network trained with Teachable Machine.

## My Classification Task
**Classes:** Rock, Paper, Scissors
**Training Images:** Rock = 46, Paper = 41, Scissors = 90
**Accuracy:** Around 40-70% - Accurate with Scissors and Rock but struggles with paper 

## How to Run
1. **Install Requirements**
```bash
pip install -r requirements.txt
```
2. **Test the Classifier**
```bash
python test_classifier.py
```
3. **Web Interface**
```bash
python web_interface.py
```
Visit http://localhost:5000

## How Computer Vision Works
### Image as Numbers
Every image is a grid of pixels. Each pixel has RGB values (0-255 for Red, Green, Blue).

### Feature Detection
The neural network learns to detect:
- **Edges**: Where colors change sharply
- **Shapes**: Combinations of edges
- **Patterns**: Repeated features
- **Objects**: Complex combinations

### My Model's Process
1. Resize image to 224x224 pixels
2. Normalize pixel values
3. Pass through neural network
4. Get probability for each class
5. Return highest probability as prediction

## Challenges I Encountered
I struggled to get the Teachable Machine algorithm to accurately categorize my test images. One major issue was that the model became biased when one category had more or clearer photos than the others. Even when I balanced the dataset with around 50 images per class, the model still misclassified most objects as paper. This was surprising because paper and rock have very different shapes, but the model seemed to latch onto small visual cues rather than the overall form. This showed me how sensitive simple machine-learning models can be to inconsistencies in the training images.

## Real-World Applications
1. **Medical**: Image classification can be used in medical imaging to help identify diseases in X-rays, MRIs, and CT scans. Models can recognize patterns that humans may miss.
2. **Security**: Computer vision is used in surveillance syustems to recognize faces, detect unusual behavior, or detect restricted objects. It can help automate threat detection.
3. **Retail**: Establishments can use image classification for inventory tracking, product scanning, and recognizing items at the self-sheckout. It can also analayze customer behavior patterns inside the store.

## Ethical Considerations
In my opinion, computer vision raises privacy concerns because cameras can constantly capture people without their awareness. Another issue is algorithmic bias, where models can misidentify certain groups of people or objects if the training data isn’t diverse or sufficient. There is also always the risk of misuse, since surveillance systems can be used in ways that violate personal freedoms or monitor people without proper consent.

## What I Learned

I learned that computer vision works by converting images into numerical data so the model can identify edges, textures, and shapes. I also learned how neural networks detect patterns layer by layer and combine those features to recognize full objects. Finally, I learned how important consistant high-quality training images are, since even small differences can affect accuracy. Overall, this project helped me to understand how the data and model architecture influence how well an image classifier preforms.
