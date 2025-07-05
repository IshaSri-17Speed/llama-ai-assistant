# 🧠 Llama.cpp-Based AI Chat Assistant

This project is a lightweight, fully local AI assistant built using [llama.cpp](https://github.com/ggerganov/llama.cpp) and a quantized Qwen1.5 0.5B GGUF model. It runs completely offline on my local machine using WSL (Ubuntu on Windows 10) — no internet or cloud required.

## ✨ Features

- 🧠 Uses **Qwen1.5-0.5B-Chat** model in `GGUF` format
- ⚡ Runs on **CPU** with no GPU required
- 💻 Built using `llama.cpp` with full CMake build system
- 🪶 Lightweight: ~4GB RAM usage with quantized Q4_K_M model
- 🌐 Works entirely **offline** after download
- 💬 Interactive CLI with conversation-style responses
- 🧰 Beginner-friendly — no prior ML experience needed

------

## ✨ What It Does

- Interactively chats like a personal assistant using a local LLM (Qwen1.5-0.5B GGUF)
- Processes user prompts in real-time via command line
- Runs efficiently on low-end hardware (8GB RAM / no GPU)
- Uses [llama.cpp](https://github.com/ggerganov/llama.cpp), a C++ inference engine optimized for speed and low memory

---

## 🔧 Tech Stack

- 💻 [llama.cpp](https://github.com/ggerganov/llama.cpp)
- 🧠 Qwen1.5-0.5B-Chat-GGUF quantized model (Q4_K_M)
- 🐧 WSL (Ubuntu 22.04) on Windows 10
- 🐙 Git, CMake, and g++ (GCC) for compilation
- 📦 Model downloaded from Hugging Face

---

## 📁 Project Structure

llama-ai-assistant/
├── models/ # GGUF model goes here
│ └── qwen1_5-0_5b-chat-q4_k_m.gguf
├── build/ # llama.cpp build output
│ └── main # Compiled binary
├── README.md # You're reading it
└── llama.cpp/ # Source code (cloned from upstream)
---

## 🚀 How to Run

1. Clone [llama.cpp](https://github.com/ggerganov/llama.cpp) and build:
    ```bash
    git clone https://github.com/ggerganov/llama.cpp.git
    cd llama.cpp && mkdir build && cd build
    cmake .. && make
    ```
2. Download the quantized model (Qwen1.5 0.5B - Q4_K_M):
    ```bash
    huggingface-cli login
    huggingface-cli download TheBloke/Qwen1.5-0.5B-Chat-GGUF \
      qwen1_5-0_5b-chat-q4_k_m.gguf \
      --local-dir ../models
    ```

3. Run the assistant:
    ```bash
    ./main -m ../models/qwen1_5-0_5b-chat-q4_k_m.gguf -i -n 512 --color
    ```

---

## 🎓 What I Learned

- How to compile and run `llama.cpp` in WSL on limited hardware
- How to download and run GGUF models offline
- Basics of memory-efficient model quantization (Q4_K_M)
- Model inference using CPU-only backends
- Structuring, documenting, and showcasing ML tools on GitHub

---

## ✅ Use Cases

- Learning LLM internals and prompt-response mechanics
- Offline chatbot with no API or cloud dependency
- Foundation for building local voice/chat assistants

---

## 🙋‍♀️ Credits

- Model by [TheBloke on HuggingFace](https://huggingface.co/TheBloke)
- llama.cpp by [ggerganov](https://github.com/ggerganov/llama.cpp)

---

## 📜 License

This project follows the licenses of the respective model and llama.cpp (MIT).

---


## Demo Screenshot 📸

![Screenshot of AI Assistant](screenshots/ai-screenshot.jfif)

## Demo Video 🎥

[Click to Watch Demo](videos/ai-assistant-demo.mp4)

