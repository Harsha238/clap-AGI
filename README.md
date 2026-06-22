# 👏 Double Clap Workspace Trigger

A lightweight Python automation tool that listens for a **double clap** through your microphone and instantly launches your preferred workspace setup.

Perfect for quickly opening applications, websites, projects, or productivity tools with a simple hands-free gesture.

## ✨ Features

* 🎤 Real-time microphone monitoring
* 👏 Detects double-clap gestures
* 🚀 Launch applications automatically
* 🌐 Open websites and dashboards
* ⚡ Lightweight and easy to customize
* 🔧 Simple Python implementation

## 📋 Requirements

* Python 3.8+
* PyAudio
* NumPy

## 📦 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/double-clap-workspace-trigger.git
cd double-clap-workspace-trigger
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### macOS Users

Install PortAudio before installing PyAudio:

```bash
brew install portaudio
```

## 🚀 Usage

Run the application:

```bash
python app.py
```

When the terminal displays:

```text
Listening for double claps...
```

simply perform two loud and distinct claps.

The script will:

1. Detect the double clap
2. Execute your configured tasks
3. Pause listening temporarily to avoid audio feedback

Stop the application anytime with:

```bash
Ctrl + C
```

## ⚙️ Customizing Tasks

Open `app.py` and locate:

```python
if clap_count == 2:
```

Add any commands you want inside this block.

### Open an Application

```python
os.system("open -a 'Spotify'")
```

### Open a Website

```python
os.system("open -a 'Google Chrome' 'https://github.com'")
```

### Open a Project in VS Code

```python
os.system("open -a 'Visual Studio Code' '/Path/To/Your/Project'")
```

### Example Workspace Setup

```python
os.system("open -a 'Google Chrome' 'https://github.com'")
os.system("open -a 'Spotify'")
os.system("open -a 'Visual Studio Code' '/Users/username/project'")
```

## 🔧 Configuration

You can adjust clap sensitivity inside `app.py`:

```python
THRESHOLD = 3000
MIN_DELAY = 0.2
MAX_DELAY = 1.0
```

| Parameter | Description                                          |
| --------- | ---------------------------------------------------- |
| THRESHOLD | Minimum sound level required to register a clap      |
| MIN_DELAY | Prevents echoes from being counted as multiple claps |
| MAX_DELAY | Maximum time allowed between two claps               |

## 📁 Project Structure

```text
double-clap-workspace-trigger/
│
├── app.py
├── requirements.txt
└── README.md
```

## 🛠 Technologies Used

* Python
* PyAudio
* NumPy

## 💡 Future Improvements

* Voice assistant integration
* Custom hotkey triggers
* Multi-clap gesture support
* Windows and Linux optimized commands
* GUI configuration panel
* Smart workspace profiles

## 📜 License

This project is open-source and available under the MIT License.

---

Made with Python and a little bit of sound magic. 👏✨
