# Project: Operationalizing Machine Learning
## Overview of the Project:
I have worked on Bank Marketing Dataset to train. I have used Microsoft Azure to configure a cloud-based machine learning production model, deploy, and consume it. After the authorization, I have created an automated ML model. Then I have deployed the best model and used Swagger API for HTTP requests to communicate with the deployed model via HTTP GET and POST requests. I have also created, publish, and consume a pipeline so that the model is publicly available and everybody can use it. 

## Architectural Diagram:
 ![arch_diagram](https://user-images.githubusercontent.com/30224144/96360454-46995d80-113f-11eb-944c-e9209f0043bc.jpg)

## Key steps:
### Automated ML Experiment:
Starting with the project, first I have selected “Registered Datasets” in ML Studio, named “Bank_Marketing” dataset. As I have worked from the Project Lab provided by Udacity, I do not have to create any service principal or authorization. Then I have selected Automated ML model for the dataset, set some parameter according to the instructions like setting experiment name, cluster name, compute power, compute type etc. It gives me best model for the dataset.
 
![1_dataset](https://user-images.githubusercontent.com/30224144/96469904-8ea7a580-124f-11eb-8e78-4f9ae5e2cd49.jpg)
![2_complete_exp](https://user-images.githubusercontent.com/30224144/96469911-91a29600-124f-11eb-96f5-00cc4f448d2f.jpg)
![3_bestmodel](https://user-images.githubusercontent.com/30224144/96469922-95361d00-124f-11eb-8618-4186ab5ad09a.jpg)

### Deploy the Best Model:
After getting the best model for the dataset, I deployed the model and named it ‘ex-deploy’. 
Application Insight Enable:
After deploying successfully, I have enabled application insights to True to monitor and log data. The following screenshots are of logs.py and Enabled Application Insights.
![4_logs py1](https://user-images.githubusercontent.com/30224144/96469939-97987700-124f-11eb-9105-79735b46a9b5.jpg)
![5_logs py2](https://user-images.githubusercontent.com/30224144/96469954-9cf5c180-124f-11eb-8d20-5f7319054c9a.jpg)


![6_app_enabled](https://user-images.githubusercontent.com/30224144/96469985-a41ccf80-124f-11eb-8614-805087f2dfea.jpg) 

### Swagger Documentation:
Swagger documentation is used to communicate via HTTP request with the model. Using Gitbash, I have enabled docker ports for swagger. I have used localhost:8001 port for swaggerapi and localhost:8003 for “ex-deploy” model.
![7_swagger](https://user-images.githubusercontent.com/30224144/96470005-a97a1a00-124f-11eb-8300-b6f80a8cf62d.jpg)


### Consume Endpoints:
After the Swagger documentation is done successfully, the model is ready to consume. From the endpoint, I can get Rest-endpoint link and key to access. If I send JSON post request via SwaggerAPI, I will get the desired output after running endpoint.py, as shown in the following screenshot.
![8_endpointoutput](https://user-images.githubusercontent.com/30224144/96470036-b3038200-124f-11eb-8b6b-d3b4086daa74.jpg)

### Creating a Pipeline:
In this step, I have uploaded the ‘aml-pipeline’ jupyter notebook file, changed the experiment and cluster name according to my project and then started executing notebook cells one by one. After a while, pipeline is created and. Then I have checked the pipeline endpoint. Following screenshots are of pipeline section, pipeline endpoint and dataset with AutoML Module.
![9_pipeline_create](https://user-images.githubusercontent.com/30224144/96470086-be56ad80-124f-11eb-9d8e-c234caed0dc2.jpg)

![10_pipeline_endpoint](https://user-images.githubusercontent.com/30224144/96470126-c4e52500-124f-11eb-8f33-1ed8fa734967.jpg)

![11_datasetautoml](https://user-images.githubusercontent.com/30224144/96470173-d4fd0480-124f-11eb-865f-1ba9604370d4.jpg)


### Publishing and Consuming a pipeline:
After the pipeline is created, I executed jupyter notebook cells to publish it from Rest-endpoint and Run widget module is also successful as shown in the screenshot. Then I published the pipeline. The following screenshots are of Published Pipeline Overview(Right hand side of the screenshot), Run details widget and scheduled run.
![12_published_pipeline_overview](https://user-images.githubusercontent.com/30224144/96470212-dd553f80-124f-11eb-9a77-00eb0f7caf04.jpg)

![13_run_details](https://user-images.githubusercontent.com/30224144/96470231-e34b2080-124f-11eb-809d-c98a61d12244.jpg)

![14_scheduled_run](https://user-images.githubusercontent.com/30224144/96470257-e8a86b00-124f-11eb-989e-2e12c8171dee.jpg)

## Screen Recording:
[Project video](https://drive.google.com/file/d/1DIefR828MBrm0Av2HArKuqnWEJCafT69/view?usp=sharing)

Here is the screen recording of my project. The pipeline endpoints are discussed here in the video.

## Points of improving project in the future:
First of all, the project lab should be improved and fast. It is slow and not comfortable to work on. Secondly, the timer of using project lab is annoying and after the laptop stops working, the timer remains on. It counts time when I am not using the project lab. I think it should be like, when I will be using project lab, it counts only that time. Thirdly, on board VMware file or process saving system should be there, so that if power cut or internet connection lost happens, it should save the on-going process of the project and can be used by the user and the process should be easy like one or two clicks away. So, users can save the time and do not have the repeat same steps again and again. Fourthly, I think in video submission, there should be only screen recording not audio. The reason is, not everyone has noise cancelling microphone and headphone, as well as, the skills of video editing. Overall, project should be interactive and knowledgeable where we can put some creativity rather than worrying about the process and submission system.
