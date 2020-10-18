# Project: Operationalizing Machine Learning
## Overview of the Project:
I have worked on Bank Marketing Dataset to train. I have used Microsoft Azure to configure a cloud-based machine learning production model, deploy, and consume it. After the authorization, I have created an automated ML model. Then I have deployed the best model and used Swagger API for HTTP requests to communicate with the deployed model via HTTP GET and POST requests. I have also created, publish, and consume a pipeline so that the model is publicly available and everybody can use it. 

## Architectural Diagram:
 ![arch_diagram](https://user-images.githubusercontent.com/30224144/96360454-46995d80-113f-11eb-944c-e9209f0043bc.jpg)




## Key steps:
### Automated ML Experiment:
Starting with the project, first I have selected “Registered Datasets” in ML Studio, named “Bank_Marketing” dataset. As I have worked from the Project Lab provided by Udacity, I do not have to create any service principal or authorization. Then I have selected Automated ML model for the dataset, set some parameter according to the instructions like setting experiment name, cluster name, compute power, compute type etc. It gives me best model for the dataset.
 
![1_dataset](https://user-images.githubusercontent.com/30224144/96360458-4dc06b80-113f-11eb-9d54-f83c81eda920.jpg)

![2_Complete_exp](https://user-images.githubusercontent.com/30224144/96360461-53b64c80-113f-11eb-9502-2996be18e101.jpg)

![3_best_model](https://user-images.githubusercontent.com/30224144/96360465-5ca71e00-113f-11eb-858d-89e6f366611e.jpg)
 
 


### Deploy the Best Model:
After getting the best model for the dataset, I deployed the model and named it ‘ex-deploy’. 
Application Insight Enable:
After deploying successfully, I have enabled application insights to True to monitor and log data. The following screenshots are of logs.py and Enabled Application Insights.
 
![4_logs1](https://user-images.githubusercontent.com/30224144/96360471-66308600-113f-11eb-9382-b7ae99c610dd.jpg)

![5_logs2](https://user-images.githubusercontent.com/30224144/96360483-73e60b80-113f-11eb-9cb2-6c1ae7ddaec2.jpg)


 ![6_app_enabled](https://user-images.githubusercontent.com/30224144/96360604-6f6e2280-1140-11eb-8cff-1ea42b0b61e5.jpg)



### Swagger Documentation:
Swagger documentation is used to communicate via HTTP request with the model. Using Gitbash, I have enabled docker ports for swagger. I have used localhost:8001 port for swaggerapi and localhost:8003 for “ex-deploy” model.

![7_swagger](https://user-images.githubusercontent.com/30224144/96360608-76953080-1140-11eb-84b4-e9dc731f9040.jpg)

### Consume Endpoints:
After the Swagger documentation is done successfully, the model is ready to consume. From the endpoint, I can get Rest-endpoint link and key to access. If I send JSON post request via SwaggerAPI, I will get the desired output after running endpoint.py, as shown in the following screenshot.
![8_endpointpy](https://user-images.githubusercontent.com/30224144/96360612-7e54d500-1140-11eb-98d4-8e2011035e0c.jpg)

### Creating a Pipeline:
In this step, I have uploaded the ‘aml-pipeline’ jupyter notebook file, changed the experiment and cluster name according to my project and then started executing notebook cells one by one. After a while, pipeline is created and. Then I have checked the pipeline endpoint. Following screenshots are of pipeline section, pipeline endpoint and dataset with AutoML Module.
![9_pipeline_created](https://user-images.githubusercontent.com/30224144/96360618-857be300-1140-11eb-95e6-214b69a9265f.jpg)
![10_pipeline_endpoint](https://user-images.githubusercontent.com/30224144/96360621-8ca2f100-1140-11eb-9e77-d8484eadf5a1.jpg)
![11_automl_dataset](https://user-images.githubusercontent.com/30224144/96360626-93316880-1140-11eb-9ed4-54f9fa9b4f98.jpg)
 
### Publishing and Consuming a pipeline:
After the pipeline is created, I executed jupyter notebook cells to publish it from Rest-endpoint and Run widget module is also successful as shown in the screenshot. Then I published the pipeline. The following screenshots are of Published Pipeline Overview(Right hand side of the screenshot), Run details widget and scheduled run.
![12_published_pipeline_overview](https://user-images.githubusercontent.com/30224144/96360631-99274980-1140-11eb-81ff-fa661aebde08.jpg)

![13_run_details](https://user-images.githubusercontent.com/30224144/96360634-9fb5c100-1140-11eb-8a18-cf2ef2e3eabf.jpg)

![14_scheduled_run](https://user-images.githubusercontent.com/30224144/96360640-a93f2900-1140-11eb-9b0e-bae4b6130dbb.jpg)

## Screen Recording:
[Project video](https://drive.google.com/file/d/1eGGXpd7rSV8WaUZuJ0l79mAijRMshuxF/view?usp=sharing)

Here is the screen recording of my project. The pipeline endpoints are discussed here in the video.

## Points of improving project in the future:
First of all, the project lab should be improved and fast. It is slow and not comfortable to work on. Secondly, the timer of using project lab is annoying and after the laptop stops working, the timer remains on. It counts time when I am not using the project lab. I think it should be like, when I will be using project lab, it counts only that time. Thirdly, on board VMware file or process saving system should be there, so that if power cut or internet connection lost happens, it should save the on-going process of the project and can be used by the user and the process should be easy like one or two clicks away. So, users can save the time and do not have the repeat same steps again and again. Fourthly, I think in video submission, there should be only screen recording not audio. The reason is, not everyone has noise cancelling microphone and headphone, as well as, the skills of video editing. Overall, project should be interactive and knowledgeable where we can put some creativity rather than worrying about the process and submission system.
