### OCR based Medical Data Extraction Project

#### Problem Statement:-

There are a lot of procedures needs to followed by the health insurance companies as per the government regulation to issue the claims, for that the insurance company has to process the images of patient details and prescription sent by hospitals or induvial doctors and extract useful data from them. For these process, the most insurance companies outsource workforce from companies like “data Analytics” to extract the information from images manually.

data Analytics uses a software, which will show the scanned images of patient details or prescription, the person needs to type the information by seeing the image manually in the the right side column and select the type of information . As it is a manual process, error will be common and dealing with the huge set of images like in the pandemic time, will not be possible with the same amount of workforce. As well the Insurance companies has requested to send the data within 24hrs when it is send for extraction. All of these constraints forced, data Analytics to consider for a software upgrade from their old software.

#### Solution:-

To solve all these problems, we are building a program which can do the extraction of data from images automatically. As always, machines can not replace humans. A person will recheck the extracted data and submit. So, that it will save a tremendous amount which was taken to type the data manually.

Here, we are using the Python programming language and pytesseract google library for extracting the data and Regex module to process the data and get distilled desired output.

#### Technologies used:-

1. Python
2. oops
3. Pdf2image module
4. Opencv
5. pytesseract
6. Regular expression
7. pytest
8. Postman
9. FastApi

#### Workflow


![image](https://github.com/user-attachments/assets/f7d8e756-6419-483f-a360-3acc31dd5807)


#### PDF to Image Convertor

Useing pdf2image library for converting PDF to image

#### Without Preprocessing Extracted Data

extracted data was not as expected.

#### Extracted data from the above image

We decided to preprocess the images using the OpenCV module before extracting data from them. As part of this process, we first applied normal thresholding, which resulted in the image shown below.


So, if there is any shadow or some noise, the normal thresholding fade out the area. which will result in loss of data.

In the search of better approach of this problem, we have decided to use adaptive thresholding technique. In this technique, the image will be divided into sub image and the thresholding value will be different for all sub regions. And the end result of adaptive thresholding is much better compared to normal thresholding.

#### After preprocessing the image data extraction



#### Notebook

For all these above trials, used jupyter books and developed the small bits of the functionalities., which can be used later while designing the class.


#### OOPS design

The code was written in using OOPs concepts for extracting the medical data from prescription and patient details documents.

#### Regular expression

Using regular expression module we can match the patterns and extract the data we want from the files. For this project, analyst the medical files and as fact all the medical documents will follow same pattern, we wrote patterns that match only the required data. Before writing the python code, It is advisable to practise and match the patterns in regex 101 website.

#### Test driven Development

In this project test driven development methodology was used to develop the code. For testing pytest module was used. For all the methods and final result the test cases was designed and checked simultaneously while developing the code.

#### FastApi

Used FastAPI for hosting the server of the project. FastApi, as name suggest is help us to develop fast and some other advantages are,

In build Data validation
In build Documentation
Fast running and performance

#### Result

This backend functionality can be integrated into the existing Analytics software, enabling automatic data extraction from images. While the extracted data may contain occasional errors, the responsible user will review, correct, and submit the final output, ensuring accuracy and reliability.

#### Benefits

One of the key benefits of this solution is that Analytics can save at least 30 seconds per document. While this may seem like a small time-saving for a single document, the cumulative effect is significant. Over time, this efficiency allows the company to process more documents within the same timeframe, ultimately boosting productivity and increasing profitability.
Since the process combines automation with manual verification, the error rate will be significantly reduced, ensuring high accuracy and reliability in the extracted data.


