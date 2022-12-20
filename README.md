# AI-102-Notes:

AI-102 is MCQ based Exam which is focused on AI related services of Azure Cloud. It has questions around SDK, API codes and various azure services. Its important to get understanding of how each services can be used and Difference between them. Ideally, We shall be good enough to use this services without needing much extrenal help if we want to pass this exam.

* Follow the official Microsoft repo of [AI-102-AIEngineer](https://github.com/MicrosoftLearning/AI-102-AIEngineer) for handson. You might need free azure trail subscription for handson.

## Azure Cognitive Service:

When we create the cognitive service resource, we gets one http endpoint and two keys(primary key and secondary key). A common practice is to use one for development, and another for production.

With `azure cli` we can list and regenerate auth keys
```cmd
 az cognitiveservices account keys list --name <resourceName> --resource-group <resourceGroup>
 az cognitiveservices account keys regenerate --name <resourceName> --resource-group <resourceGroup> --key-name key1
```

## Text Analytics
* has `detect_language` method to `TextAnalyticsClient`

## Computer Vision vs Face Service:
While the Computer Vision service offers basic face detection (along with many other image analysis capabilities), the Face service provides more comprehensive functionality for facial analysis and recognition.

One of the most fundamental capabilities of the Face service is to detect faces in an image, and determine their attributes, such as head pose, blur, the presence of spectacles, and so on.

Optical character recognition (OCR) is a subset of computer vision that deals with reading text in images and documents. 

The Read API uses a newer text recognition model and generally performs better for larger images that contain a lot of text, but will work for any amount of text. It also supports text extraction from .pdf files, and can recognize both printed text and handwritten text in multiple languages.

The Read API uses an asynchronous operation model, in which a request to start text recognition is submitted; and the operation ID returned from the request can subsequently be used to check progress and retrieve results.
