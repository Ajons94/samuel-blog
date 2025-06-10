# Assignment 3: My LLM Project

## Introduction
For this assignment, I explored how to deploy and use two types of large language models (LLMs): an online model and a local model. My goal was to set them up, integrate them into my coding environment, and see how they could help with programming tasks. I chose Qwen from Silicon Flow for the online model and Ollama for the local model. I tested both, compared them, and even tried a bonus task to see how an LLM could assist with research. Below, I've included a summary of every step I took, the results, and my thoughts.

## 1. Online Model API
- **Model Selected:** Qwen from Silicon Flow
- **Setup Process:**
  - I started by visiting cloud.siliconflow.cn and signing up for an account. After logging in, I found the API section and generated my API key, which I saved securely in a private file.
  - Next, I installed Python on my computer by downloading it from python.org. I checked it worked by typing `python --version` in my terminal, and it showed Python 3.12.
  - I then installed the "requests" library to connect to the API. In my terminal, I ran the command `pip install requests` successfully.
  - To test it, I opened VSCode, created a new file called `test_Qwen.py`, and wrote a simple program to ask Qwen for a Python function. Here’s what I used:
    ```python
    import requests

    api_key = "sk-ly.............dpjp"
    url = "https://api.siliconflow.cn/v1/completions"
    headers = {"Authorization": f"Bearer {api_key}"}
    data = {
        "model": "Qwen/Qwen2.5-72B-Instruct",
        "prompt": "Write a simple Python function to say hi",
        "max_tokens": 100
    }
    response = requests.post(url, json=data, headers=headers)
    print(response.json()["choices"][0]["text"])
    ```
  - I ran the file with `python test_Qwen.py` in the terminal.
- **Results:** It worked! The output was a clean Python function:
  ```
  def say_hi():
      print("Hi!")
  ```
  I was thrilled to see Qwen respond so quickly and accurately.

## 2. Local Model Deployment
- **Model Selected:** Ollama with llama3
- **Setup Process:**
  - I visited ollama.com and downloaded the installer for my system (I use Windows). The installation was straightforward. I just followed the prompts.
  - In my terminal, I typed `ollama --version` to confirm it was installed, and it showed the version number.
  - I chose the "llama3" model because it’s small and suitable for my laptop. I downloaded it by running `ollama pull llama3` in the terminal, which took a few minutes.
  - To test it, I ran `ollama run llama3` and typed, "Write a simple Python function to say hi."
- **Results:** Success! The terminal displayed:
  ```
  def say_hi():
      print("Hi!")
  ```
  It felt great to have a model running right on my computer, even if it was a bit slower than the online option.

## 3. Integration into Development Environment
- **Environment:** VSCode
- **Process:**
  - I downloaded VSCode from code.visualstudio.com and installed it. I created a new folder called "LLM_Assignment" for my project.
  - For the online model, I made a file named `online_Qwen.py` in VSCode. I reused my earlier code but changed the prompt to "Write a Python function to find the area of a rectangle." I ran it by right-clicking and selecting "Run Python File in Terminal."
  - The result was:
    ```
    def rectangle_area(length, width):
        return length * width
    ```
  - For the local model, I created `local_ollama.py`. I wrote this code:
    ```python
    import requests
    response = requests.post('http://localhost:11434/api/generate',
                            json={"model": "llama3", "prompt": "Write a Python function to find the area of a rectangle."})
    print(response.json()['response'])
    ```
  - I started Ollama in a terminal with `ollama run llama3`, then ran my file in VSCode.
  - The result was similar:
    ```
    def rectangle_area(length, width):
        return length * width
    ```
  - To test their usefulness, I gave both a buggy code: `def area(length, width): return length * widht` (with a typo: "widht"). I edited my prompts to "Fix this: def area(length, width): return length * widht" and ran both files.
- **Results:** Both caught the typo! Qwen and Ollama suggested changing "widht" to "width," proving they’re helpful for debugging code. I was impressed by how they assisted my programming.

## 4. Comparison of Models
- **Online Model (Qwen):**
  - **Strengths:** Very fast response, easy to set up, and user-friendly. The API call took just seconds.
  - **Weaknesses:** Needs a stable internet connection, and I worry about costs if I use it a lot.
- **Local Model (Ollama with llama3):**
  - **Strengths:** Works offline, so it’s private and free once set up. I liked not needing the internet.
  - **Weaknesses:** Slower than Qwen, and my laptop got warm. it might need a stronger computer for bigger tasks.
- **My Thoughts:** Qwen was faster and smoother, which I loved for quick tasks. But Ollama felt safer for private work since it’s offline. I’d use Qwen for speed and Ollama when I’m not connected.

## 5. Exploring Research Workflows
- **Task:** I tried using Qwen to summarize a short text for a research-like task.
- **Process:**
  - I created a file called `text.txt` with a simple paragraph: "I love to code. It’s fun. I learn new things every day and enjoy solving problems."
  - I wrote a new file, `bonus.py`, to ask Qwen to summarize it:
    ```python
    import requests
    api_key = "sk-ly.............dpjp"
    url = "https://api.siliconflow.cn/v1/completions"
    headers = {"Authorization": f"Bearer {api_key}"}
    with open('text.txt', 'r') as file:
        text = file.read()
    data = {
        "model": "Qwen/Qwen2.5-72B-Instruct",
        "prompt": f"Summarize this: {text}",
        "max_tokens": 100
    }
    response = requests.post(url, json=data, headers=headers)
    print(response.json()["choices"][0]["text"])
    ```
  - I saved both files, ran the code, and got a result.
- **Results:** Qwen replied: "Coding is fun and educational, involving daily learning and problem-solving." It worked well and was easy to set up, but it missed the personal tone of “I love to code.” I found it useful for quick summaries, though I’d check for missing details in real research.

## Conclusion
This project was an exciting journey! I successfully set up Qwen from Silicon Flow and Ollama with the llama3 model. Both worked in VSCode, helping me write and fix Python code, like a rectangle area function and a typo in my script. 
Qwen was fast and convenient, while Ollama was great offline. The bonus task showed me how an LLM can summarize text, which could help with schoolwork or research. 
I learned a lot about coding, models, and troubleshooting, and I’m proud of my progress. Next, I’ll add this report to my Assignment 2 website to share my work!
