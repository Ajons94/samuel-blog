# Assignment 4: Developing an Application with the Aid of LLM

- **Student Name: Ajoniloju Samuel Olatunde**
- **Student Number: LS2425227**

## Background and Functionality

Picture this: you’re a farmer, staring at your corn fields, wondering if they’re healthy or about to catch some nasty disease. That’s where my **Crop Health Estimator** app comes in, a tool I built to make farming smarter and easier! I wanted to create something that takes data from drones or satellites (like soil moisture or temperature) and turns it into clear advice for farmers. This app isn’t just a school project, it’s a game-changer for anyone growing crops!

So, what does it do? Let me break it down:
- **Health Check**: You plug in data like moisture (0-100%), temperature (-50 to 50°C), and vegetation scores (0-10). The app cranks out a health score and labels your crops as “Excellent,” “Good,” “Fair,” or “Poor.”
- **Risk Alerts**: It spots dangers, like fungal diseases, and warns you to act fast.
- **AI Advice**: Using SiliconFlow’s awesome AI, it gives tips, like “Water your wheat more” or “Check for pests.”
- **Chat Mode**: You can ask questions, like “How do I save my sick corn?” and the AI types answers letter by letter, like it’s chatting live!
- **Log It**: Everything scores, risks, advice, chats saves to a file for later.

I designed this for farmers using remote sensing tech, which is all about checking crops from the sky. It’s like having a farming expert on your computer, ready to help 24/7!

But building it wasn’t a walk in the park. The big challenges were:
- **Coding Smarts**: I’m new to Python, so writing code to handle multiple fields and complex logic was like learning to juggle.
- **AI Magic**: Connecting to SiliconFlow’s AI meant figuring out APIs, which felt like wiring a spaceship at first.
- **Typing Effect**: Making the AI’s answers type out live took extra work to get the timing just right.
- **.exe Drama**: Turning my code into a clickable .exe file hit a snag with a permission error that had me scratching my head.

These hurdles made the project tougher but way more rewarding when I nailed it!

## Development Environment

I built this app on my trusty Lenovo laptop, nothing fancy, but it got the job done. Here’s the setup:
- **Hardware**: A laptop with 16GB RAM, Intel Core i7, and a 512GB SSD.
- **Operating System**: Windows 11 Pro, version 22H2.
- **Tools and Compilers**:
  - Python 3.13.4: The main language for coding.
  - PyInstaller 6.14.1: To turn my code into a .exe file.
  - Requests library (version 2.31.0): For talking to SiliconFlow’s AI.
  - Visual Studio Code: My go-to editor for writing and debugging code.
- **AI Model**: SiliconFlow’s Qwen/Qwen2-7B
- **Helper**: I got some brainstorming and bug-fixing tips from Google and Grok.

This setup was simple but powerful enough to bring my app to life. I worked mostly at my desk, fueled by coffee and late-night snacks!

## Development Process

Building this app was like crafting a cool gadget—part planning, part coding, and part problem-solving. Here’s how it went down:

1. **Planning the App**: I started with a big idea: an app to help farmers using remote sensing data. I jotted down features—health scores, risk alerts, AI advice, and a chat mode. I wanted it to feel fun, so I added a typing effect for the AI’s answers.

2. **Coding the Basics**: I used Python to write code that asks for crop data (wheat, corn, or rice) and calculates health scores. I added logic for multiple fields, disease risks, and trends (like “Your fields are mostly healthy!”). This took a while since I’m new to coding, but I kept tweaking until it worked.

3. **Linking it Up the AI**: I signed up for SiliconFlow, grabbed an API key, and added code to send crop data to their AI. I was thrilled when it sent back advice like “Increase irrigation for South Field!” I also made the answers type out slowly, which took some trial and error to get the speed right.

4. **Interactive Q&A**: I added a feature where users can ask questions, like “How do I prevent fungi?” The AI uses the crop data to give smart answers, and I made sure it typed them out for that live-chat vibe.

5. **Making the .exe**: My assignment needed a .exe file, so I used PyInstaller. But I hit a “PermissionError” when it couldn’t overwrite an old .exe. I chatted with Grok, who suggested closing programs, deleting old files, and running PowerShell as admin. After a few tries, I got a working `crop_health.exe`!

6. **Testing Like Crazy**: I tested with fake data—two corn fields, one healthy, one not. I checked scores, risks, AI advice, and Q&A. I also made sure the log file saved everything. Grok helped me debug a few glitches, like when the AI didn’t respond (turned out my internet was off!).

This process was a mix of coding, learning, and fixing bugs, but seeing the app come together was so exciting!

## Results

The Crop Health Estimator works like a charm, and I’m stoked to show it off! I tested it with two corn fields:
- **North Field**: 60% moisture, 25°C, veg score 7. Result: “Good, keep it up!” with a score of 72/100. Risk: Low.
- **South Field**: 30% moisture, 40°C, veg score 4. Result: “Poor, add water fast!” with a score of 38/100. Risk: High (fungal disease alert!).

The SiliconFlow AI gave awesome advice: “Improve drainage for South Field and monitor for fungi.” When I asked, “How do I fix South Field?” it typed out, “Increase irrigation and apply fungicides soon.” The typing effect made it feel like a real conversation!

Here’s a screenshot of the app in action:

![App Screenshot](https://raw.githubusercontent.com/Ajons94/samuel-blog/374abc4e620f60f7218a4a218bc3bf50d9eecd7f/Crop%203.jpeg)
*Caption: My app showing corn field results and the AI typing out advice!*

Another screenshot shows the Q&A:

![Q&A Screenshot](https://raw.githubusercontent.com/Ajons94/samuel-blog/374abc4e620f60f7218a4a218bc3bf50d9eecd7f/Crop%201.jpeg)
*Caption: Asking the AI how to save my crops, with answers typing out live!*

The log file (`CropHealthLog.txt`) saved everything—scores, risks, advice, and chats—perfect for keeping records.

## Source Code

Want to check out my code or try the app yourself? I’ve uploaded it to GitHub for everyone to see:

[Download Source Code](https://github.com/Ajons94/Crop-Health-Estimator/blob/main/crop_health.py)

[Executable Downloadable Link](https://github.com/Ajons94/Crop-Health-Estimator/blob/main/crop_health.exe)

---

This app is my proudest project yet. It’s not just about getting a good grade—it’s about helping farmers grow better crops with tech. Building it was a wild ride, from coding to battling .exe errors, but every step was worth it.

*— Samuel, Future Farming Innovator*
