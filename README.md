# homelab

Asus spec:
- CPU: i7 6th gen
- RAM: 16GB
- SSD: 120GB
- VRAM: 4GB

After init-nvidia role run restart might be help.

```
# for GPU
helm repo add nvdp https://nvidia.github.io/k8s-device-plugin
helm repo update
helm install nvdp nvdp/nvidia-device-plugin --namespace kube-system

# for GUI
helm install open-webui open-webui/open-webui -f helm/ai/values.yaml
```