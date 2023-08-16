
# Heart Rate Measurement in the Cloud Using AWS

The goal is to design a system that allows a contactless method of measuring the heart rate with
simultaneous multisampling in real-time using commodity hardware like a webcam and ambient light
with the intention to generate data points which can be combined with various others to create a data
model for illness detection.

## INTRODUCTION

Commercial heart rate monitors utilize near-infrared light to determine the heart rate by comparing the
reflection of hemoglobin in the blood. The same principle can be applied at a distance using ambient light and
an image sensor by analyzing and observing changes in color in the forehead region. The current state of this
technology is experimental. Its scope is limited to running on a single machine and working with a single
subject. Our work intends to scale this to be used for multiple subjects in real-time using cloud technologies.

## Tools Used

### Hardware

- Webcam

### Cloud Tools

- AWS Lambda – data processing, application logic
- AWS Kinesis – video and data streaming
- AWS Rekognition – face recognition and identification of facial landmarks (for isolating faces)
- AWS Sagemaker – heart rate estimation
- AWS S3 – image storage
- AWS DynamoDB – result storage
- AWS SQS – data pipeline optimization (experiment)

### Other Tools/Libraries

- Python v3.5+
- OpenCV v2+
- NumPy, SciPy
- Various ML libraries for testing SpO2 models

## Architecture

![Architecture](https://github.com/kkapoor3/Heart-rate-AWS/blob/main/extracted_image_1_0.png)

