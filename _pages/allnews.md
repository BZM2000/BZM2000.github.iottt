---
title: "组内动态 | 张圆教授课题组 | 沈阳建筑大学"
layout: textlay
excerpt: "组内动态 | 张圆教授课题组 | 沈阳建筑大学"
sitemap: false
permalink: /allnews.html
---

# 组内动态

{% for article in site.data.news %}

<p>{{ article.date }} <br>
<em>{{ article.headline }}</em></p>
{% endfor %}

<!DOCTYPE html>
<html>
<head>
    <title>GPT-3.5 Turbo Model Chatbot</title>
    <script src="https://cdn.jsdelivr.net/npm/openai-js@2.2.1/dist/openai.js"></script>
    <script>
      const openai = new OpenAI('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');
    </script>
</head>
<body>
    <h1>GPT-3.5 Turbo Model Chatbot</h1>
    <p>Type your message below to start chatting:</p>

    <div id="chatbot-window">
        <div id="user-input">
            <input type="text" id="user-message" placeholder="Type your message here..."/>
            <button type="button" id="submit-button">Submit</button>
        </div>
        <div id="chatbot-messages">
        </div>
    </div>

    <script>
        document.getElementById('submit-button').addEventListener('click', async () => {
            const userMessage = document.getElementById('user-message').value;
            document.getElementById('user-message').value = '';

            const chatbotResponse = await openai.engines.engine('davinci').query({
                query: userMessage,
            });

            const messageBox = document.getElementById('chatbot-messages');
            const newMessageDiv = document.createElement('div');
            newMessageDiv.innerHTML = '<div><strong>You:</strong> ' + userMessage + '</div><div><strong>Chatbot:</strong> ' + chatbotResponse.data.choices[0].text + '</div>';
            messageBox.appendChild(newMessageDiv);
        });
    </script>
</body>
</html>
