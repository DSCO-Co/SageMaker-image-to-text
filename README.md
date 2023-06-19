# SageMaker-image-to-text
A starter Jupyter notebook that deploys the Salesforce/ blip-image-captioning-base model to an endpoint. 


This Jupyter notebook outlines a procedure for creating and deploying an AWS SageMaker endpoint using a Hugging Face model. The model is designed to perform image captioning tasks based on the given inputs.

# What is Done in this Notebook:

Installation of the necessary packages including PyTorch, transformers, git-lfs, and SageMaker.

Setting up the SageMaker session and retrieving the SageMaker execution role.

Creation of an inference script (inference.py) which includes:

model_fn: A function to load the model and processor from the Hugging Face Hub.
predict_fn: A function to perform the prediction task. It performs both conditional and unconditional image captioning based on the given input.

Cloning the Hugging Face repository that contains the trained model.

Preparation of a model.tar.gz archive which includes the model, the processor, and the inference code.

Use of HuggingFaceModel class from SageMaker to create a model instance.

Deployment of the model as a SageMaker endpoint.

Example of how to make a prediction using the deployed endpoint.

A method to invoke the SageMaker endpoint using the SageMaker runtime client.

# How to Use:

To use this notebook, you would need to have your AWS account set up, and the necessary permissions for running SageMaker instances, S3 operations, and IAM operations.

The inference script provided needs to be tailored according to the model's requirements and the prediction task you want to perform.

Ensure to replace the repository variable with the Hugging Face repository that contains your model.

When you are ready to make a prediction, replace the data dictionary with the input to your model.

# Important Note:

When creating a notebook instance make sure that is has enough ESB Storage. The sample notebook here needs at least 10 gb. 

The cost associated with the usage of AWS resources will apply. Make sure to stop or delete any endpoints that are not in use to avoid unnecessary charges.

Please be aware that this notebook was developed with the following versions and may not work with different versions:

transformers version: 4.26
PyTorch version: 1.13
Python version: 3.9

Always check the compatibility of your versions with the AWS SageMaker and the model you're trying to deploy.