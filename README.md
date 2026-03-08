This project demonstrates how to use LangChain with Google Gemini (Generative AI) to generate responses and perform simple tasks like translation using Python.

🚀 Project Overview

This notebook shows how to:

Install LangChain with Google Generative AI support

Connect to Google Gemini model

Send prompts to the model

Generate responses

Perform English → Odia translation

🛠️ Technologies Used

Python

LangChain

Google Generative AI (Gemini)

Jupyter Notebook

Installation

Install the required library:

pip install -U "langchain[google-genai]"
Set API Key

Set your Google API Key before running the model.

import os
os.environ["GOOGLE_API_KEY"] = "YOUR_API_KEY"
🤖 Initialize the Model
from langchain.chat_models import init_chat_model

model = init_chat_model("google_genai:gemini-2.5-flash-lite")
💬 Generate a Response

Example prompt:

response = model.invoke("About Odisha")
print(response)
🌍 Translation Example

This example translates English text into Odia.

from langchain_core.messages import HumanMessage, SystemMessage

message = [
    SystemMessage("Translate the following from English into Odia language"),
    HumanMessage("Good things are coming your way")
]

response = model.invoke(message)
print(response)
