<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Etta AI</title>
  <style>
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      background-color: #f0f2f5;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .chat-container {
      width: 100%;
      max-width: 450px;
      height: 700px;
      background-color: #ffffff;
      border-radius: 16px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
      display: flex;
      flex-direction: column;
      overflow: hidden;
      position: relative;
    }

    .chat-header {
      background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
      color: white;
      padding: 20px;
      border-top-left-radius: 16px;
      border-top-right-radius: 16px;
      text-align: center;
      position: relative;
    }

    .menu-button {
      position: absolute;
      right: 20px;
      top: 20px;
      font-size: 1.5em;
      cursor: pointer;
    }

    .dropdown-menu {
      display: none;
      position: absolute;
      top: 60px;
      right: 20px;
      background: #ffffff;
      border: 1px solid #ccc;
      border-radius: 8px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
      z-index: 10;
    }

    .dropdown-menu.active {
      display: block;
    }

    .dropdown-menu select {
      margin: 10px;
      padding: 6px;
      width: 90%;
    }

    .chat-box {
      flex-grow: 1;
      padding: 20px;
      overflow-y: auto;
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .chat-message {
      display: flex;
      flex-direction: column;
      max-width: 85%;
    }

    .chat-message.user {
      align-self: flex-end;
      align-items: flex-end;
    }

    .chat-message.etta {
      align-self: flex-start;
      align-items: flex-start;
    }

    .message-bubble {
      padding: 12px 18px;
      border-radius: 22px;
      line-height: 1.4;
    }

    .user .message-bubble {
      background: #007bff;
      color: white;
      border-bottom-right-radius: 4px;
    }

    .etta .message-bubble {
      background-color: #e9e9eb;
      color: #333;
      border-bottom-left-radius: 4px;
    }

    .chat-input-area {
      display: flex;
      padding: 10px 20px;
      border-top: 1px solid #ddd;
      background-color: #f8f9fa;
    }

    #userInput {
      flex-grow: 1;
      border: 1px solid #ccc;
      border-radius: 20px;
      padding: 10px 18px;
      font-size: 1em;
      outline: none;
    }

    #sendButton {
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 50%;
      width: 44px;
      height: 44px;
      margin-left: 10px;
      cursor: pointer;
      font-size: 1.5em;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    #sendButton:hover {
      background-color: #0056b3;
    }

    .loading-bar {
      width: 0;
      height: 4px;
      background: #007bff;
      transition: width 15s linear;
      position: absolute;
      top: 0;
      left: 0;
    }
  </style>
</head>
<body>
  <div class="chat-container">
    <div class="loading-bar" id="loadingBar"></div>
    <div class="chat-header">
      <h2>Etta AI</h2>
      <div class="menu-button" id="menuToggle">⋮</div>
      <div class="dropdown-menu" id="dropdownMenu">
        <select id="themeSelector">
          <option value="light">Light Mode</option>
          <option value="dark">Dark Mode</option>
        </select>
        <select id="languageSelector">
          <option value="en">English</option>
          <option value="fr">Français</option>
          <option value="es">Español</option>
        </select>
      </div>
    </div>

    <div class="chat-box" id="chatBox"></div>

    <form class="chat-input-area" id="chatForm">
      <input type="text" id="userInput" placeholder="Ask me anything..." />
      <button type="submit" id="sendButton" aria-label="Send Message">➤</button>
    </form>
  </div>

  <script>
    const chatForm = document.getElementById('chatForm');
    const userInput = document.getElementById('userInput');
    const chatBox = document.getElementById('chatBox');
    const loadingBar = document.getElementById('loadingBar');
    const menuToggle = document.getElementById('menuToggle');
    const dropdownMenu = document.getElementById('dropdownMenu');
    const themeSelector = document.getElementById('themeSelector');
    const languageSelector = document.getElementById('languageSelector');

    menuToggle.addEventListener('click', () => {
      dropdownMenu.classList.toggle('active');
    });

    themeSelector.addEventListener('change', (e) => {
      document.body.style.backgroundColor = e.target.value === 'dark' ? '#121212' : '#f0f2f5';
    });

    chatForm.addEventListener('submit', async (event) => {
      event.preventDefault();
      const userText = userInput.value.trim();
      if (!userText) return;

      addMessage(userText, 'user');
      userInput.value = '';

      startLoadingBar();
      const response = await getEttaResponse(userText);
      stopLoadingBar();
      addMessage(response, 'etta');
    });

    function addMessage(text, sender) {
      const messageDiv = document.createElement('div');
      messageDiv.className = `chat-message ${sender}`;
      const bubbleDiv = document.createElement('div');
      bubbleDiv.className = 'message-bubble';
      bubbleDiv.textContent = text;
      messageDiv.appendChild(bubbleDiv);
      chatBox.appendChild(messageDiv);
      chatBox.scrollTop = chatBox.scrollHeight;
    }

    function startLoadingBar() {
      loadingBar.style.width = '0';
      setTimeout(() => {
        loadingBar.style.width = '100%';
      }, 10);
    }

    function stopLoadingBar() {
      setTimeout(() => {
        loadingBar.style.width = '0';
      }, 15000);
    }

    async function getEttaResponse(message) {
      const lower = message.toLowerCase();
      if (['hello', 'hi', 'hey', 'greetings'].some(g => lower.startsWith(g))) {
        return "Hello! It's a pleasure to chat with you. How can I be of service?";
      } else if (lower.includes("who created you")) {
        return "I was created by AGBOR RENE ETTA.";
      } else if (lower.includes("when were you born") || lower.includes("created")) {
        return "My functions were launched on July 31, 2025.";
      } else {
        return await callDuckDuckGoSearch(message);
      }
    }

    async function callDuckDuckGoSearch(query) {
      try {
        const response = await fetch(`https://api.duckduckgo.com/?q=${encodeURIComponent(query)}&format=json&no_redirect=1&no_html=1`);
        const data = await response.json();

        if (data.Abstract && data.Abstract !== "") {
          return `${data.Abstract}\n🔗 ${data.AbstractURL}`;
        }

        if (data.RelatedTopics && data.RelatedTopics.length > 0) {
          const topic = data.RelatedTopics.find(t => t.Text && t.FirstURL);
          if (topic) {
            return `${topic.Text}\n🔗 ${topic.FirstURL}`;
          }
        }
return `I couldn't find an exact answer, but you can try searching here:\n🔍 https://duckduckgo.com/?q=${encodeURIComponent(query)}`;
      } catch (error) {
        console.error("DuckDuckGo API error:", error);
        return "⚠️ I had trouble fetching an answer. Please try again later but make sure you are connected to the internet.";
      }
    }
  </script>
</body>
</html>
