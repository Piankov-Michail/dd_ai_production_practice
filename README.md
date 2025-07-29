# dd_ai_production_practice

### Запуск flowise: <br><br> <pre>gzip -d flowise_custom_preset.tar.gz</pre> <pre>docker load -i flowise_custom_preset.tar</pre> <pre>docker run -d --network=host flowise_custom_preset:latest</pre> <br>
### NVIDIA CUDA: <br><br> <pre>sudo apt install -y docker-ce nvidia-container-toolkit</pre> <pre>sudo apt update && sudo apt upgrade -y</pre>
### Запуск Ollama с Qwen3 1.7B: <br><br> <pre>docker run -d --network=host --gpus=all -v ollama:/root/.ollama --name ollama ollama/ollama</pre> <pre>docker exec -d -it ollama ollama run qwen3:1.7b</pre> <pre>docker exec -d -it ollama ollama pull nomic-embed-text:v1.5</pre> <br>
### Запуск телеграм-бота: <br><br> <pre>docker build -t ai-bot .</pre> <pre>docker run -it --rm --network=host ai-bot</pre>
