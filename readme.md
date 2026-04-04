
# Héberger des LLM en local via Docker 

## Modèle gratuits

* Llama 3 (par Meta)

* CodeLlama (llama 2 par Meta)

* Qwen (Alibaba, certains modèles distribués librement)

* Gemma (Google / DeepMind)

* Mistral open-source

# Ollama - documentation

https://ollama.com/blog/ollama-is-now-available-as-an-official-docker-image

https://docs.ollama.com/docker

https://github.com/ollama/ollama

# Ollama  
docker pull ollama/ollama

# CPU only
docker run -d -p 11434:11434 --name ollama ollama/ollama

# Nvidia GPU
docker run -d --gpus=all -p 11434:11434 --memory=16g --memory-swap=16g --name ollama -v C:\Users\nelo9\ollama-data:/root/.ollama ollama/ollama serve


# Pull a model inside the container
docker exec -it ollama ollama pull qwen2.5-coder
docker exec -it ollama ollama pull qwen3-coder
docker exec -it ollama ollama pull deepseek-coder-v2

# Run a model inside the container

docker exec -it ollama ollama run qwen2.5-coder
docker exec -it ollama ollama run qwen3-coder
docker exec -it ollama ollama run deepseek-coder-v2

# open-webui

# tout supprimer 
docker rm -f ollama && docker rmi -f ollama/ollama

# URL 
http://localhost:11434


# Attention avec la configuration de l'antivirus (bitdefender)
Gerer les execption sur  :

c:\dev\data

c:\programdata\dockerdesktop

c:\users\nelo9\.continue

c:\users\nelo9\.docker

c:\users\nelo9\.vscode

c:\users\nelo9\appdata\local\docker

C:\Users\nelo9\ollama-data

# continue.dev cli

## Installation
npm i -g @continuedev/cli

## Lancement

cn --config %userprofile%/.continue/config.yaml
