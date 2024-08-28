# MonReader - Mobile Document Digitization for Everyone
## Overview
MonReader is an innovative mobile application designed to provide a seamless document digitization experience for everyone, particularly the blind and visually impaired, researchers, and individuals needing efficient, high-quality, and bulk document scanning. The app automatically detects page flips from a low-resolution camera preview, captures high-resolution images, recognizes document corners, crops and dewarps the images, enhances text contrast, and performs text recognition with formatting preserved. The entire process is driven by MonReader's machine learning-powered redactor, ensuring an accurate and accessible digital copy of the document.

## Background and Motivation
In the era of digitization, accessibility and efficiency are paramount. Despite the availability of numerous document scanning apps, many fall short when it comes to catering to the specific needs of blind users or providing the high-speed, high-quality scanning required for bulk digitization. MonReader was developed to address these gaps. It combines artificial intelligence and computer vision to offer a truly hands-free scanning experience, where users only need to flip the pages, and the app does the rest.

The technology behind MonReader reflects our company's broader mission: to make artificial intelligence and computer vision accessible to everyone. We believe in machines that can see and understand the world, packed into small, intelligent devices that easily integrate into existing workflows. With MonReader, we bring this vision to document digitization, ensuring that high-quality scanning is available to everyone, regardless of their technical expertise or physical abilities.

## Datasets
The MonReader project utilizes a specialized dataset of page-flipping videos collected from smartphones. The dataset is crucial for training the machine learning models that detect page flips, ensuring the app can operate effectively in real-world scenarios. Here’s an overview of the dataset:

- `Source`: Videos recorded using smartphones, capturing the action of page flipping.
- `Labeling`: Videos are labeled based on whether they contain a page-flipping action or not.
- `Processing`: The videos are clipped into short segments, with each segment labeled as flipping or not flipping. Extracted frames from these videos are saved to disk in sequential order, following the naming - -structure: VideoID_FrameNumber.
#### Dataset Structure
- `Flipping Videos`: Videos and corresponding frames where a page flip is occurring.
- `Non-Flipping Videos`: Videos and corresponding frames where no page flip is occurring.
## Milestones
The development of MonReader follows a structured plan with key milestones aimed at ensuring the application meets its goals effectively. Here’s a breakdown of the major milestones:

### Dataset Collection and Preprocessing:

Collect a diverse set of page-flipping videos from various smartphones.
Label the dataset accurately, ensuring each video segment is correctly classified as flipping or not flipping.
Preprocess the data by clipping videos, extracting frames, and organizing them with a consistent naming structure.
### Model Development:

Develop and train a machine learning model to predict page flipping from single images with a focus on maximizing the F1 score.
Implement a secondary model to analyze sequences of images for more accurate flipping detection over time.
### Application Integration:

Integrate the trained models into the MonReader mobile application.
Develop the image processing pipeline to handle tasks such as corner detection, cropping, dewarping, contrast enhancement, and text recognition.
### Testing and Optimization:

Conduct extensive testing of the MonReader application across various devices and lighting conditions.
Optimize the app for speed, accuracy, and user experience, ensuring it meets the needs of all users, especially those who are visually impaired.
### Deployment and User Feedback:

Launch the MonReader application on major mobile platforms.
Collect user feedback to identify areas for improvement and implement updates accordingly.
Success Metrics
The primary metric for evaluating the success of MonReader is the F1 score, particularly in the context of page-flip detection from single images. A higher F1 score indicates better model performance in distinguishing between flipping and non-flipping actions. Additionally, the app's overall usability, speed, and accuracy in real-world scenarios will be critical indicators of its success.

#### Bonus Objectives
As a stretch goal, we aim to enhance MonReader’s capabilities by predicting whether a given sequence of images contains a page-flipping action. This would improve the app’s accuracy in more challenging scenarios and further streamline the document digitization process.

*MonReader is not just a tool; it’s a step towards making document digitization accessible and efficient for everyone. With cutting-edge AI and computer vision technology, we are transforming how documents are scanned and digitized, one page flip at a time.*
