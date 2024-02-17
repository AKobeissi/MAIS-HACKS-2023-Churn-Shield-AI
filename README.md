# ChurnSheild AI - MAIS-HACKS-2023
## Inspirations
As Management students studying Mathematics, we were eager to try and use **Artificial Intelligence** and **Machine Learning** applied to current business issues. Among many issues that we discussed, customer churn seemed to be a relevant problem seen by numerous companies, where not enough is being done to prevent it. For that reason we created **ChurnShield**, our AI powered solution to try and decrease customer churn rates in companies, and help them maintain their customers!

## What it does
**ChurnShield** is an AI powered solution that performs two main functions. First, it uses advanced machine learning models that accurately predicts at risk customers who are at a **high risk of churn**. Second, it uses**Llama2**, a Large Language Model that artificially generates loyalty programs and promotional messages specific to each customer based on their data. By creating custom loyalty programs and messages, our solution decreases customer churn rates, saves money, and promotes growth for your organization! 
## How we built it
We built this solution in Python. The libraries that we used were scikit-learn for our machine learning models used in our predictive stage. We formed the predicative stage of this solution as a binary classification problem, so we ran numerous classification models such as **Logistic Regression, Support Vector Machines, Decision Trees, and LightGBM**. After predicting the high risk customers, we created a pipeline that tags the at risk customers and filters them into a secondary data frame. Using this secondary data frame as our data, we trained and fine-tuned Llama2, an LLM, using its API from HuggingFace as well as **LangChain** to generate specific content for each customer. The data we used comes from Kaggle, the data is coming from a bank where they have tracked relevant data to predict churn. The target variable is "Exited", meaning that customer has left the bank. So using this data, we made the predictions, and then fed the predicted customers into out LLM to generate personalized loyalty programs with interest rates to help them stay. 
## Challenges we ran into
Some of the challenges we ran into was finding the right LLM to use, given that a lot of API's have a fee to them, we wanted to find a free, open-source, LLM that has a good performance, this took a lot of research but we ended up settling on Llama2. We also had issues with the output of the LLM, it provided very variant and poor results at first, so we had to learn how to prompt engineer and how to use different methodologies for Language Models such as LangChain. When trying to figure out how to use LangChain with out model, we also encountered issues with memory and storage, notably we had tried using the GPU provided by google colab but it had run out of free credits. For this reason we were only able to get output for 10 customers. We also had issues in terms of running some of the predictions since some of the data was textual, but we overcame it by learning some new NLP processing techniques!
## Accomplishments that we're proud of
We are proud of being able to use and implement a Generative AI model by ourselves for the very first time! We are also proud of the work we did to make our idea into an actual project!
## What we learned
We learnt a lot about different types of Language Models and how to implement them. We learnt that LangChain is an incredibly important library to use when creating these models and how we can fine-tune and get customized outputs using it. We also learned how to run various machine learning models, and data visualization! 
## What's next for ChurnShield
Whats next for us is to try and improve the accuracy of our prediction models and implementing a time feature to our data. In terms of the GenAI, we are also excited to improve the outputs, get more personalized messages, and scale the solution to for thousands of customers.
