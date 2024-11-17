
GENERATIONAL AI , 
PDF SCANNER , AND AI  ANALYZER / RESPONDER. 



Using , Neo4J,  
	Ollama, 
	Streamlit, and 
 	Docker. 









This is a fork from the repository  - https://github.com/craig-osterhout/docker-genai-sample

From the OFFICIAL DOCKER DOCS  , located here  - https://docs.docker.com/guides/use-case/genai-pdf-bot/

- This version is working as of  09/16/2024 - 




------------------------------------

Running the application. 


- To run the aplication properly , your device must meet the following prerequisites. 

 1. Docker running on the machine  
 2 . Neo4j Docker image running , by pulling the official Neo4j image from Docker hub  , and running it on port
      - "7474:7474"
      - "7687:7687"
  -- To see if you have it connected properly , you may visit localhost:7474 to see if it is running , 
      - While it is running in docker container , and you should see a site displaying its content. 
3. Ollama in a Dockerized container must also be running on port 11434. 
  -- To see if you have it connected properly , you may visit localhost:11434 to see if it is running , 
      - While it is running in docker container , and you should see a site displaying its content. 



4. With neo4j and Ollama hooked up and configured properly , after running them in docker , 
  you should be able to run  

docker compose up --build    

and build and run the project from there. 




---------------------------------------------------------------
-----------------------------------------------
-------------------------------
-----------------
-----------
----
-
-



Updates 
_____________________________________________________________________________

- Updated the requirements.txt file  , through a variation of a .venv and retesting. 

- Intialized a dockerfile , using dockerinit ,   selcting the following variations. 
		- Python 	
		- 3.12 
           	-Listening on port: - 8000		
 What is the command to run your app?: -  streamlit run app.py --server.address=0.0.0.0 --server.port=8000 

- Updated the compose.yaml to hold the proper settings to connect to a local containerized Neo4j Database and Ollama server


- Ran and tested the application using a local , 
	docker containerized Neo4j container and a Ollama LLM model container , both running concurrently.
--------------------------------------------------------------------------------------------------------------------

--- You should be running both containers , like this image on the right. 

![Screenshot (543)](https://github.com/user-attachments/assets/62942ff2-793b-40d7-8920-f72e233964a6) 

These other images with Neo4j Aura Cloud services , and running a Ollama locally  OUT of docker , is NOT what this repo is configured for ,  

This is configured to run your ollama inside of docker from docker hub.  Ok ?  kk - 
But enjoy the screenshots provided below ! 
![Screenshot (542)](https://github.com/user-attachments/assets/c3c676bf-7c74-4f3d-89d8-765d6b5ddba8)
![Screenshot (541)](https://github.com/user-attachments/assets/1cae76ea-8116-4ba7-820e-465d26721473)
![Screenshot (540)](https://github.com/user-attachments/assets/bfdb3d10-b070-491b-a590-ae5e6574ade2)
![Screenshot (539)](https://github.com/user-attachments/assets/f549fcb9-a72e-444e-bb7c-2d6bb24aa536)
![Screenshot (538)](https://github.com/user-attachments/assets/782bfca8-3d76-414a-a812-fa13e032c315)
![Screenshot (537)](https://github.com/user-attachments/assets/654641b2-9c76-498e-8398-2a1458102a43)
![Screenshot (545)](https://github.com/user-attachments/assets/dcc34c0d-e650-454e-a62e-9aef9b6b1480)
![Screenshot (544)](https://github.com/user-attachments/assets/1bc98a89-37f2-47d7-a9bb-4b701942e501)





 NOTICE  ,  after running docker compose up --build  , something similar to  this ^ is what your container should have running in it. 







----------------------------------------------------------------------------------------
# docker-genai-sample

A simple GenAI app for [Docker's Docs](https://docs.docker.com/) based on the [GenAI Stack](https://github.com/docker/genai-stack) PDF Reader application.
