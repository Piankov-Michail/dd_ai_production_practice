# dd_ai_production_practice

### Запуск flowise: <br><br> <pre>docker run --network=host flowiseai/flowise</pre> <br>
### Запуск Ollama с Qwen3 1.7B: <br><br> <pre> docker run -d --network=host --gpus=all -v ollama:/root/.ollama --name ollama ollama/ollama && sleep 5 && docker exec -it ollama ollama run qwen3:1.7b && docker exec -it ollama ollama run nomic-embed-text:v1.5</pre> <br>
### Запуск телеграм-бота: <br><br> <pre>python3 -m venv ai_bot_env</pre> <pre>source ai_bot_env/bin/activate</pre> <pre>sudo apt-get update && sudo apt-get install -y ffmpeg</pre> <pre>pip install -r requirements.txt</pre> <pre>python bot.py</pre>
