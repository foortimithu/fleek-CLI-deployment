
# Fleek CLI Deployment Guide

## 1. Install Node.js (if not already installed)
```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install -y nodejs
```

## 2. Install Fleek CLI globally
```bash
sudo npm install -g @fleek-platform/cli
```

---

## Deploying a Static Site with Fleek

### 3. Log in to Fleek
```bash
fleek login
```
> Open the URL in a browser and complete the login.

### 4. Create a new project (optional)
```bash
fleek projects create
```
> If this fails, proceed — you may already have a default project.

### 5. Set up your site folder
```bash
mkdir ~/fleek-site
cd ~/fleek-site
echo "Hello World" > index.html
```

### 6. Initialize Fleek site configuration
```bash
fleek sites init
```
- Select your project
- Name your site (e.g., `my-fleek-site`)
- For directory input, type `.` (dot for current folder)
- Choose `no` for optional build command
- Save config as `JSON`

### 7. Deploy your site
```bash
fleek sites deploy
```

### 8. View live site
Check the output for your unique Fleek URL, like:
```
🔗 https://your-site-name.on-fleek.app
```

---

## Bonus Commands

### List all projects
```bash
fleek projects list
```

### List all sites
```bash
fleek sites list
```

### Upload a file to Fleek storage
```bash
fleek storage upload ./myfile.png
```
