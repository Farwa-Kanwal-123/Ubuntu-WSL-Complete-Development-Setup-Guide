# Ubuntu-WSL-Complete-Development-Setup-Guide
This document covers the complete setup of a development environment in Ubuntu (WSL), including Node.js (via NVM), npm, Python, and pip. It is based on the exact steps we followed and common issues we resolved.

1. Install Node.js inside WSL (Recommended)

Update packages
sudo apt update

Install Node.js (LTS)
sudo apt install -y nodejs npm

Verify installation
node -v
npm -v
2. Installing Node.js 20 Using NVM (Best Practice)

We use NVM (Node Version Manager) because it allows easy switching between Node versions.
Step 2.1: Install NVM
curl -fsSL https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
Step 2.2: Reload Terminal
source ~/.bashrc
Step 2.3: Verify NVM Installation
nvm --version
3. Install & Upgrade Node.js to Version 20
Step 3.1: Install Node.js v20
nvm install 20
Step 3.2: Use Node.js v20
nvm use 20
Step 3.3: Set Node.js 20 as Default
nvm alias default 20
Step 3.4: Verify Node & npm
node -v
npm -v
4. Installing Python, pip, and Virtual Environment

Ubuntu does not always come with Python and pip pre-installed.
Step 4.1: Install Python & pip
sudo apt install -y python3 python3-pip python3-venv
Step 4.2: Verify Python & pip
python3 --version
pip3 --version
Step 4.3: Create virtual environment
python3 -m venv venv
Step 4.4: Activate
source venv/bin/activate
5. Enable python and pip Commands (Optional but Recommended)

By default, Ubuntu uses python3 and pip3. To enable python and pip:
sudo apt install -y python-is-python3
Verify
python --version
pip --version
6. Fixing Common Errors
❌ command not found: node

✔ Node.js was not installed or NVM was not loaded

Solution:
source ~/.bashrc
nvm use 20
❌ pip: command not found

✔ pip was not installed or only pip3 exists

Solution:
sudo apt install python3-pip
sudo apt install python-is-python3
7. Copy & Paste in Ubuntu Terminal
Paste

    Ctrl + Shift + V
    Right-click → Paste

Copy

    Ctrl + Shift + C

    In Windows Terminal (WSL), Ctrl + V also works.

8. Final Verification Checklist

Run these commands to confirm everything is set up correctly:
node -v
npm -v
nvm --version
python --version
pip --version

If all commands return versions → ✅ setup is complete.
9. Recommended Tools

    Windows Terminal (Best for WSL)
    VS Code + WSL Extension
    NVM for Node version control
    python-venv for Python projects

✅ Setup Completed Successfully

Your Ubuntu (WSL) environment is now fully ready for:

    Frontend (Next.js, React)
    Backend (FastAPI, Node.js)
    Python development
    npm & pip package management

Happy Coding 🚀
