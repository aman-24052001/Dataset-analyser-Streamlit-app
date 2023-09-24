# Dataset-analyser-Streamlit-app
# using OpenAI LLM to analyze csv files


Streamlit CSV Analyzer
![image](https://github.com/aman-24052001/Dataset-analyser-Streamlit-app/assets/97305123/ecb93050-d4fd-41a0-a840-5e873fc07f6f)


Streamlit CSV Analyzer is a simple web application built with Streamlit
that allows users to upload a CSV file and perform data analysis queries on it.
Users can input queries, and the application will use OpenAI's language model to provide responses based on the uploaded CSV data.

# Streamlit:

Streamlit is a popular Python library used for creating web applications with minimal code. It allows developers to build interactive web interfaces quickly.
In the code, the application starts with importing Streamlit as 'st'. The 'st' object is used to create various UI elements like titles, headers, file uploaders, text areas, buttons, and more.

# OpenAI's Language Model (LLM):

OpenAI's language model is used in this application to perform natural language processing tasks. It's used for interpreting user queries and providing responses based on the data uploaded in a CSV file.
The OpenAI model is initialized using the OpenAI class from the langchain.llms module.
Working of the App:

# Title and File Upload:

The app starts by displaying a title and a header using st.title and st.header.
Users are prompted to upload a CSV file using st.file_uploader. This uploaded CSV file will be used for data analysis.
# Query Input:

Users can enter their analysis queries in a text area using st.text_area. This query will be used as input for the language model.
Generate Response:

A button labeled "Generate Response" is provided (st.button) to trigger the analysis based on the uploaded CSV data and the user's query.
When the user clicks this button, the application sends the CSV data and the query to the query_agent function.
query_agent Function:

The query_agent function is responsible for processing the user's query and providing a response.
Inside this function, the uploaded CSV data is read and converted into a Pandas DataFrame using pd.read_csv.
An agent is created using create_pandas_dataframe_agent from the LangChain library. This agent will use the OpenAI language model for understanding the query and performing actions on the data.
The agent.run(query) method is called with the user's query, which triggers the analysis.
The result of the analysis is then returned and displayed in the Streamlit app using st.write.

# Dependencies:

The app has a few external dependencies listed at the end of the code,
such as 'dotenv', 'langchain', 'pandas', 'openai', and more. These libraries are required for various functionalities within the app.




