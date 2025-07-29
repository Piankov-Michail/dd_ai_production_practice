# dd_ai_production_practice

### Intro: [chat example](https://htmlpreview.github.io/?https://github.com/Piankov-Michail/dd_ai_production_practice/blob/main/ChatExport/messages.html)

### Запуск flowise: <br><br> <pre>gzip -d flowise_custom_preset.tar.gz</pre> <pre>docker load -i flowise_custom_preset.tar</pre> <pre>docker run -d --network=host flowise_custom_preset:latest</pre> <br>
### NVIDIA CUDA: <br><br> <pre>sudo apt install -y docker-ce nvidia-container-toolkit</pre> <pre>sudo apt update && sudo apt upgrade -y</pre>
### Запуск Ollama с Qwen3 1.7B и nomic-embed-text для эмбеддингов: <br><br> <pre>docker run -d --network=host --gpus=all -v ollama:/root/.ollama --name ollama ollama/ollama</pre> <pre>docker exec -d -it ollama ollama run qwen3:1.7b</pre> <pre>docker exec -d -it ollama ollama pull nomic-embed-text:v1.5</pre> <br>
### Установить TELEGRAM_TOKEN и BOT_USERNAME в bot.py
### Запуск телеграм-бота: <br><br> <pre>docker build -t ai-bot .</pre> <pre>docker run -it --rm --network=host ai-bot</pre>
