# dd_ai_production_practice

### Запуск flowise: <br><br> <pre>gzip -d flowise_custom_preset.tar.gz</pre> <pre>docker load -i flowise_custom_preset.tar</pre> <pre>docker run --network=host flowise_custom_preset:latest</pre> <br>
### NVIDIA CUDA: <br><br> <pre>sudo apt install -y docker-ce nvidia-container-toolkit</pre> <pre>sudo apt update && sudo apt upgrade -y</pre>
### Запуск Ollama с Qwen3 1.7B: <br><br> <pre>docker run -d --network=host --gpus=all -v ollama:/root/.ollama --name ollama ollama/ollama</pre> <pre>docker exec -d -it ollama ollama run qwen3:1.7b</pre> <pre>docker exec -d -it ollama ollama pull nomic-embed-text:v1.5</pre> <br>
### Запуск телеграм-бота: <br><br> <pre>python3 -m venv ai_bot_env</pre> <pre>source ai_bot_env/bin/activate</pre> <pre>sudo apt-get update && sudo apt-get install -y ffmpeg</pre> <pre>pip install -r requirements.txt</pre> <pre>python bot.py</pre>
