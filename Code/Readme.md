# How to use this notebook and the data?
First, go to the url provided and press download. Any data can be used in this model, just make sure the data can be used in the model.

Then, download the model.py, this is a sample code used for analyzing the car information. Any code can be used, just make sure it's in line with SALib's requirement.

Lastly, rename your downloaded file as "car_information.csv", name in the code can also be changed. You can run this data on your own computer!

### Brief introduction to SALib
SALib, or Sensitivity Analysis Library, is a powerful and versatile Python library used for conducting sensitivity analysis. Sensitivity analysis is a fundamental tool in data science and decision-making that helps assess the influence of input parameters on model outputs. SALib provides a range of techniques to perform global and local sensitivity analysis on models or simulations, making it valuable for a wide array of applications.

The library offers support for various sensitivity analysis methods, such as Sobol, Morris, FAST, and more. It allows users to quantify the importance of different input factors, detect nonlinear interactions, and understand the robustness of models. SALib is particularly useful in fields like environmental modeling, finance, engineering, and machine learning, where understanding parameter sensitivities and their impact is crucial.

SALib simplifies the sensitivity analysis process, making it accessible to both researchers and practitioners, and it is widely adopted in the data science community for enhancing model interpretability and decision-making.

### Data query and analysis process
In this piece of code, we directly import the data downloaded from the website, which is linked at the end of this paper, and then analyze this piece of data using the model.py file in order to simulate the decision-making process of an AI in reality. We then analyze this decision-making process using morris imported from SALib, and we end up with a dot plot that covers all the parameters in a set, which shows us the most heavily weighted of all the parameters.

### Abstract

<img src="Interpretable Machine Learning for Autonomous Vehicles_ Bridging the Gap with eXplainable Artificial Intelligence (XAI) (3).png" alt="Abstract Word Cloud">
