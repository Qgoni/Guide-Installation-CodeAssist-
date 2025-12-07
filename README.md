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
### 3. Add Docker's GPG key
```bash
curl -fsSL https://  download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
### 4. Add Docker repository
```bash
sudo add-apt-repository "deb [arch=amd64] https://  download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```
### 5. Update packages again (after adding new repo)
```bash
sudo apt update
```
### 6. Install Docker components
```bash
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
### 7. Install UV package manager
```bash
curl -LsSf https://  astral.sh/uv/install.sh | sh
```
### 8. Load UV to PATH
```bash
source $HOME/.local/bin/env
```
### 9. Clone CodeAssist repository
```bash
git clone https://github.com/gensyn-ai/codeassist.git
```
### 10. Navigate to project directory
```bash
cd codeassist
```
### 11. Run CodeAssist using UV
```bash
uv run run.py
```
