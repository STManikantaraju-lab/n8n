# Install n8n on Docker Container

# 1. Install Docker Desktop 
Download from Docker Desktop for Windows. \
Install it, then restart your computer if asked.  \
Open Docker Desktop and make sure it says “Docker Engine is running.”

# 2. Open PowerShell (or CMD) as Administrator

# 3. Pull the official n8n image 
docker pull n8nio/n8n

# 4. Create a local folder for n8n data (so your workflows are saved) 
mkdir C:\n8n   or you can set the folder for n8n workflow folder where need to set

# 5. Run the n8n container (Windows-friendly version) 
docker run -it --rm -p 5678:5678 -v C:\n8n:/home/node/.n8n n8nio/n8n   \
🔎 Explanation:  \
-p 5678:5678 → maps port 5678 so you can open n8n in your browser.   \
-v C:\n8n:/home/node/.n8n → mounts your Windows folder C:\n8n to store workflows.

# 6. Open n8n in your browser   
Go to 👉 http://localhost:5678
