# dd_ai_production_practice

### Intro: [chat example](https://htmlpreview.github.io/?https://github.com/Piankov-Michail/dd_ai_production_practice/blob/main/ChatExport/messages.html) <br>
### Diagram:
### ![Diagram](https://github.com/Piankov-Michail/dd_ai_production_practice/blob/main/diagram.jpg) <br>
---
### Launch flowise (ready-made docker image with chatflow installed): <br><br> 
```bash
gzip -d flowise_custom_preset.tar.gz

docker load -i flowise_custom_preset.tar
docker run -d --network=host flowise_custom_preset:latest
```
### NVIDIA CUDA: <br><br> 
```bash
#sudo apt purge -y docker-ce nvidia-container-toolkit

sudo apt install -y docker-ce nvidia-container-toolkit
sudo apt update && sudo apt upgrade -y
```
### Launch Ollama with Qwen3 1.7B and nomic-embed-text for embeddings: <br><br> 
```bash
docker run -d --network=host --gpus=all -v ollama:/root/.ollama --name ollama ollama/ollama
docker exec -d -it ollama ollama run qwen3:1.7b</pre> <pre>docker exec -d -it ollama ollama pull nomic-embed-text:v1.5
```
### Set values TELEGRAM_TOKEN and BOT_USERNAME in bot.py <br>
### Launch telegram-bot: <br><br> 
```bash
docker build -t ai-bot
docker run -d -it --rm --network=host ai-bot
```
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
#### [Pinepone for Document store](https://www.pinecone.io)
