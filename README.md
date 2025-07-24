# dd_ai_-production_practice

### Запуск flowise: ```docker run --network=host flowiseai/flowise```
### Запуск Ollama с Qwen3 1.7B: ```docker run -d --network=host --gpus=all -v ollama:/root/.ollama -p 11434:11434 --name ollama
ollama/ollama && sleep 5 && docker exec -it ollama ollama run qwen3:1.7b```
### Запуск телеграм-бота: 
```python3 -m venv ai_bot_env```
```source ai_bot_env/bin/activate```
```sudo apt-get update && sudo apt-get install -y ffmpeg```
```pip install -r requirements.txt```
```python bot.py```
