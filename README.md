# dd_ai_production_practice

### Intro: [chat example](https://htmlpreview.github.io/?https://github.com/Piankov-Michail/dd_ai_production_practice/blob/main/ChatExport/messages.html) <br>
### Diagram:
### ![Diagram](https://github.com/Piankov-Michail/dd_ai_production_practice/blob/main/diagram.jpg) <br>
---
### Launch flowise (ready-made docker image with chatflow installed): <br><br> <pre>gzip -d flowise_custom_preset.tar.gz</pre> <pre>docker load -i flowise_custom_preset.tar</pre> <pre>docker run -d --network=host flowise_custom_preset:latest</pre> <br>
### NVIDIA CUDA: <br><br> <pre>sudo apt purge -y docker-ce nvidia-container-toolkit</pre> <pre>sudo apt install -y docker-ce nvidia-container-toolkit</pre> <pre>sudo apt update && sudo apt upgrade -y</pre>
### Launch Ollama with Qwen3 1.7B and nomic-embed-text for embeddings: <br><br> <pre>docker run -d --network=host --gpus=all -v ollama:/root/.ollama --name ollama ollama/ollama</pre> <pre>docker exec -d -it ollama ollama run qwen3:1.7b</pre> <pre>docker exec -d -it ollama ollama pull nomic-embed-text:v1.5</pre> <br>
### Set values TELEGRAM_TOKEN and BOT_USERNAME in bot.py <br>
### Launch telegram-bot: <br><br> <pre>docker build -t ai-bot .</pre> <pre>docker run -d -it --rm --network=host ai-bot</pre>
---
### [Chatflow](https://github.com/Piankov-Michail/dd_ai_production_practice/blob/main/Chatflow.json) for custom importation <br>
### [Data for RAG in Chatflow (q_a format)](https://github.com/Piankov-Michail/dd_ai_production_practice/blob/main/q_a.txt)
---
### Links:
#### Google custom search
* [Programmable Search (get Programmable Search Engine ID)](https://programmablesearchengine.google.com)
* [Google Custom Search Api Key](https://developers.google.com/custom-search/v1/overview?hl=ru)
#### [Ollama](https://ollama.com)
#### [Docker Installation and Docks](https://docs.docker.com/engine/install/ubuntu)
#### [Pinecpone for Document store](https://www.pinecone.io)
