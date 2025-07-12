## 🛠 Installation & Setup

### 📁 Step 1: Set Up Your Project Folder

Create a folder named `task3-style-transfer` and place the following files inside:
- `content.jpg` — your content image
- `style.jpg` — your style image
- `coding.ipynb` — the main notebook
- `README.md` — this documentation


### 🐍 Step 2: Create and Activate Virtual Environment (Recommended)

#### For **Windows**:
```bash
python -m venv env
env\Scripts\activate
```

#### For **MacOS**:
```bash
python3 -m venv env
source env/bin/activate
```

### Step 3: Install Required Packages
```bash
pip install torch torchvision matplotlib pillow
pip freeze > requirements.txt
```

Requirements.txt
```bash
torch
torchvision
matplotlib
pillow
```

### Step 4: Run the Style Transfer

Inside the notebook:
   - Adjust the content_weight, style_weight, and steps as needed
   - Run the final cell to view and save the stylized output (output.jpg)

### Step 5: Run the script