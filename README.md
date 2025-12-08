# Guide-Installation-CodeAssist
## Follow step by step

### 1. Update System Packages
```bash
sudo apt update
```
### 2. Install required dependencies
```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```
### 3. Installing  Docker
```bash
sudo apt update && sudo apt install ca-certificates curl -y && \
sudo install -m 0755 -d /etc/apt/keyrings && \
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo tee /etc/apt/keyrings/docker.asc > /dev/null && \
sudo chmod a+r /etc/apt/keyrings/docker.asc && \
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && \
sudo apt update && \
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
```
### 4. Install UV package manager
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```
### 5. Load UV to PATH
```bash
source $HOME/.local/bin/env
```
### 6. Clone CodeAssist repository
```bash
git clone https://github.com/gensyn-ai/codeassist.git
```
### 7. Navigate to project directory
```bash
cd codeassist
```
### 8. Run CodeAssist using UV
```bash
uv run run.py
```
<img width="2537" height="1365" alt="image" src="https://github.com/user-attachments/assets/da5c8079-6fab-4a06-8a4e-37e168f6b6a9" />
