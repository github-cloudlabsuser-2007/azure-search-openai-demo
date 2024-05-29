# app/backend

## Overview

The `app/backend` directory contains the backend code for the application. It is built using [Quart](https://quart.palletsprojects.com/), a Python framework for asynchronous web applications. The backend communicates with the frontend using the AI Chat App HTTP Protocol.

## Structure

The main entry point of the backend is the `app.py` file. This file sets up the Quart application, configures the routes, and initializes various services such as Azure Storage, Azure Search, and OpenAI.

The `approaches` directory contains the classes powering the Chat and Ask tabs. Each class uses a different RAG (Retrieval Augmented Generation) approach. The approaches include:

- `ChatReadRetrieveReadApproach`
- `ChatReadRetrieveReadVisionApproach`
- `RetrieveThenReadApproach`
- `RetrieveThenReadVisionApproach`

## Customization

You can customize the backend by modifying the `app.py` file or the classes in the `approaches` directory. For example, you can change the `system_message_chat_conversation` variable in the `ChatReadRetrieveReadApproach` class to match your data.

## Running the Backend

To run the backend, you need to have Python installed. You can then install the required dependencies using pip:

```sh
pip install -r requirements.txt