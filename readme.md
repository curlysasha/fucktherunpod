cd

wget -O /workspace/stable-diffusion-webui/models/Stable-diffusion/azov2.safetensors https://civitai.com/api/download/models/38589

wget -P /workspace/stable-diffusion-webui/models/VAE/ https://huggingface.co/stabilityai/sd-vae-ft-mse-original/resolve/main/vae-ft-mse-840000-ema-pruned.ckpt

wget -P /workspace/stable-diffusion-webui/models/ControlNet/ https://huggingface.co/lllyasviel/ControlNet-v1-1/resolve/main/control_v11p_sd15_canny.pth

wget -P /workspace/stable-diffusion-webui/models/ControlNet/ https://huggingface.co/lllyasviel/ControlNet-v1-1/resolve/main/control_v11f1e_sd15_tile.pth

git clone https://github.com/curlysasha/fucktherunpod.git

cd fucktherunpod
unzip embeddings.zip -d /workspace/stable-diffusion-webui/embeddings
cp -r webui-user.sh /workspace/stable-diffusion-webui/webui-user.sh
cp -r azov2.json /workspace/stable-diffusion-webui/models/Stable-diffusion 

pip install insightface
pip install ultralytics
pip install onnxruntime


git clone https://github.com/Bing-su/adetailer.git /workspace/stable-diffusion-webui/extensions/adetailer

git clone https://github.com/Gourieff/sd-webui-reactor.git /workspace/stable-diffusion-webui/extensions/sd-webui-reactor
git clone https://github.com/adieyal/sd-dynamic-prompts.git /workspace/stable-diffusion-webui/extensions/sd-dynamic-prompts
git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui-wildcards.git /workspace/stable-diffusion-webui/extensions/stable-diffusion-webui-wildcards

wget -P /workspace/stable-diffusion-webui/models/insightface https://github.com/facefusion/facefusion-assets/releases/download/models/inswapper_128.onnx

cd /workspace/stable-diffusion-webui/extensions/sd-webui-controlnet
git pull

apt install unzip
cd
wget https://files.pythonhosted.org/packages/83/6a/27d221e7ff0cccf490a460cdb1c559b278d0ae2acec53d365ed3c706ef9f/dynamicprompts-0.29.0-py2.py3-none-any.whl
python -m pip install dynamicprompts-0.29.0-py2.py3-none-any.whl
pip install -U dynamicprompts

cd /workspace/
source venv/bin/activate
python -m pip install -U pip
pip uninstall -y onnx onnxruntime onnxruntime-gpu onnxruntime-silicon onnxruntime-extensions
pip install onnx==1.14.1 onnxruntime==1.15.1

#ПОМЕНЯТЬ НАСТРОЙКИ ДИНАМИК ПРОМТОВ []
#ПОМЕНЯТЬ НАСТРОЙКИ КЕШ КОНТРОЛНЕТ

#ПЕРЕЗАГРУЗИТЬ
