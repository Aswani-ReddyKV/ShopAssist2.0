# ShopAssist 2.0 

## 1. Project Overview :: 
ShopAssist 2.0 is an innovative chatbot which got developed to provide a good experience w.r.to online shopping. Here user is looking out for buying a laptop and our chatbot is going to help user in narrowing down on the different options present and provide recommendations. 

This chatbot combines the power of LLMs(Large Language models) and rule base functions to get an accurate information. 

## 2. Problem Statement
We are given a dataset (in the form of .csv file) which has all the details about different laptops having their configurations, usage issues, brand names, budget etc. We need to build a chatbot which provides recommendations to users based on their requirements. 

## 3. Key Objectives 
Here are the key objectives of this project :: 
* User Interaction 
* Parse given dataset and have relevant information 
* Based on user inputs, query and get user requirements  

## 4. Approach 

* Conversation and Information Gathering: The chatbot will utilize language models to understand and generate natural responses. Through a conversational flow, it will ask relevant questions to gather information about the user’s requirements. 

    * Determine the user's requirements::  For simplicity, we have used 6 features to encapsulate the user's needs.  

        * The 6 features are as follows: -  

            * GPU intensity 
            * Display quality  
            * Portability  
            * Multitasking  
            * Processing speed  
            * Budget 
* Information Extraction: Once the essential information is collected, rule-based functions come into play, extracting the top three laptops that best match the user’s needs. 

* Personalized Recommendation: Leveraging this extracted information, the chatbot engages in further dialogue with the user, efficiently addressing their queries and aiding them in finding the perfect laptop solution. 

## 5. High Level System Design 

ShopAssit 2.0 is built using client-server architecture. For user interaction chatbot is provided on web browser which will be interacting with OpenAI LLM for having conversations, moderations, and provides recommendations to users based on their requirements. Flask framework is used to host chatbot on web based platform 


## 6. Project Stages  
This project is divided into three stages: 

* Stage 1: Intent Clarity and Confirmation 
* Stage 2: Product Mapping and Information Extraction 
* Stage 3: Product Recommendation 
The Flask application utilizes various functionalities:

#### Stage 1: Intent Clarity and Confirmation :: 

This stage involves initiating and managing the conversation between the user and the AI system. 

Key Functions: 

- `initialize_conversation()`: Starts the conversation with the user. 
- `get_chat_completions()`: Continuously processes user inputs and generates LLM responses. 
- `moderation_check()`: Flags and halts conversations containing unsafe or sensitive content. 
#### Stage 2: Product Mapping and Information Extraction :: 

This stage filters laptops based on user requirements and identifies the top recommendations. 

Key Functions: 

- `product_map_layer()`: Extracts and maps key features (e.g., GPU intensity, display quality) from the dataset. 
- `compare_laptops_with_user()`: Matches user requirements against the laptop features to calculate scores. 
- `recommendation_validation()`: Validates the recommendations to ensure they meet quality thresholds. 


#### Stage 3: Product Recommendation ::  

This stage delivers recommendations and engages in further conversation. 

Key Functions: 

- `initialize_conv_reco()`: Generates a structured conversation with summarized laptop recommendations. 
- `get_chat_completions()`: Facilitates follow-up queries and detailed discussions about the recommended laptops. 


## 7. Prerequisites
- Python 3.7+
- OpenAI API Key

## 8. Screenshot

User output example screenshot:



