<!-- PROJECT LOGO -->
<br />
<p align="center">
  <p align="center">
    <img src="images/haliya-cover.png" alt="haliya title" width="600" height="auto">
  </p>

  <p align="center">
    Haliya is an AI Fortune Teller Bot integrated inside a website. It is especially designed for the students of PLM. Haliya offers six main categories; path, lovelife, grades, health, decision maker, and a mini game professor guesser (only PLM Computer Science professors)
    <br />
</p>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#-about-the-project">About The Project</a>
      <ul>
        <li><a href="#-features">Features</a></li>
        <li><a href="#-showcase">Showcase</a></li>
      </ul>
    </li>
    <li>
      <a href="#-getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#-disclaimer">Disclaimer</a></li>
    <li><a href="#-developers">Developers</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

## 💡 About The Project

This repository contains the source code for Haliya, an AI Fortune Teller Chatbot for students around Pamantasan ng Lungsod ng Maynila (PLM). Developed as a submission for our finals project in the course Application Development and Emerging Technologies, this project showcases our creativity and skills using frontend and backend technologies.

### **🔮 Features**

- User-friendly UI and UX
- NLP (Both Filipino and English)
- Speech-recognition
- Emotion Changer (Haliya based on feedback)
- Generative AI (speech, natural language, and image)
- PLM scope learning


### **📸 Showcase**

**Main UI:**

https://github.com/Yuyuhiei/Haliya-The-AI-Fortune-Teller/assets/149577447/4ae055c4-f167-449f-af5b-fc2906eadbcb

**Main feature (The main five categories):**

https://github.com/Yuyuhiei/Haliya-The-AI-Fortune-Teller/assets/149577447/110fc712-3bcc-4c62-8a4d-a78f1194cbf6

**Prof-guesser:**

https://github.com/Yuyuhiei/Haliya-The-AI-Fortune-Teller/assets/149577447/86ad4d4b-a8e4-41a6-b72f-d62e154ac5ce

**Screenshots**
![main ui](https://github.com/Yuyuhiei/Haliya-The-AI-Fortune-Teller/assets/149577447/3b2f0138-81b9-4090-992e-ffde3b69a6c8)
![Main Chat](https://github.com/Yuyuhiei/Haliya-The-AI-Fortune-Teller/assets/149577447/2f8ea026-9ec2-41a1-8593-6407c30fb5ea)
![prof-guesser](https://github.com/Yuyuhiei/Haliya-The-AI-Fortune-Teller/assets/149577447/d3698558-f1b2-48d1-95c0-784de2879aaa)

## **⚙ Technology Used**

- **Client:** React
- **Server:** Node, Flask, Rasa
- **Programming Languages:** JavaScript, Python
- **Tools:** Figma, OpenAI API

## 🆕 Getting Started

- ### **Prerequisites**
  - Any web browser
  - <a href="https://nodejs.org/en">Node.js</a>
  - <a href="https://www.python.org/downloads/release/python-31011/">Python 3.10.11</a>

<!-- GETTING STARTED -->

- ### **Installation**

1. **Clone repository**

   ```bash
   git clone https://github.com/vinnyy-ph/Haliya-The-AI-Fortune-Teller.git
   ```

2. **Change the directory to the repository and setup the environment**:

    ```bash
    cd C:\ADET AI Exhibit
    ```
    ![image](https://github-production-user-asset-6210df.s3.amazonaws.com/86844554/331859116-7e230d5c-167f-48be-8667-55e93c74c05a.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240623%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240623T102513Z&X-Amz-Expires=300&X-Amz-Signature=d0202dca3a983c1d3b10512cee96d713a0c02b2a342f2d7ba70c5d662caa255f&X-Amz-SignedHeaders=host&actor_id=113322585&key_id=0&repo_id=802780933)    
    - **Create python virtual env by running** 
      ```bash
      python -m venv .venv
      ```
    - **Go to .venv** 
      ```bash
      cd .venv
      ```

    - **Run virtual env activation script** 
      ```bash
      .\Scripts\activate
      ```

    - **NOTE:** Ensure that your IDE is using the virtual environment's (.venv) interpreter. 
        - in VS Code, this is done by running `>Python: Select Interpreter` in the command palette, and selecing the `.venv` environment.    

    - **Install python backend reqs** 
      ```bash
      pip install -r requirements.txt
      ```
    - **Install node.js frontend reqs**
        ```bash
        cd client
        npm install
        ```
    - **Train the RASA model by opening a terminal**
        ```bash
        cd .venv/prof-guesser
        rasa train
        ```

3. **Host the frontend server**:

   ```bash
   cd client
   npm run dev
   ```
   ![image](https://github-production-user-asset-6210df.s3.amazonaws.com/86844554/331941621-dab99563-6a07-4c45-af69-c0b30fc95f93.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240623%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240623T103922Z&X-Amz-Expires=300&X-Amz-Signature=497f434996d124ce35f7f1d322908651a161b01ee6b654e6ade24686f532dedb&X-Amz-SignedHeaders=host&actor_id=113322585&key_id=0&repo_id=802780933)  
   React frontend will now be hosted at localhost:5173

   - **Host flask server**
      ```bash
      cd .venv
      python main.py
      ```
   - **Host RASA server**
      ```bash
      // Open a new terminal
      cd .venv/prof-guesser
      rasa run actions
      ```
      ```bash
      // Open a new terminal
      cd .venv/prof-guesser
      rasa run --cors "*" --enable-api
      ```
      
      Flask server will now be hosted at localhost:5000;
      ![image](https://github-production-user-asset-6210df.s3.amazonaws.com/86844554/331859647-3c1b2d40-c359-426f-9ed9-0088a0eb697f.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240623%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240623T104120Z&X-Amz-Expires=300&X-Amz-Signature=66af4c724c12127a449faeb41341fa61e33dea55724d98f350cc390d71d6473a&X-Amz-SignedHeaders=host&actor_id=113322585&key_id=0&repo_id=802780933)

    ### 📝 API Key config  
    - Add OpenAI API key as an Environment variable under `OPENAI_API_KEY`  
    - Python will access this value with `os.environ['OPENAI_API_KEY']`


## ❗❗ Disclaimer

This project was developed as part of our coursework for Application Development and Emerging Technologies at Pamantasan ng Lungsod ng Maynila (PLM). It is intended for educational purposes only and may not be suitable for production use.

Updates and Maintenance: This project was created as a one-time submission for a course requirement. As such, we may not actively maintain or update the repository. However, we welcome forks and further development by the community.

## 👥 Developers

<b>🐐 GOATED Group

- [@gekiiMei](https://github.com/gekiiMei)
- [@vinnyy](https://github.com/vinnyy-ph)
- [@alexong04](https://github.com/alexong04)
- [@bonitoflakes101](https://github.com/bonitoflakes101)