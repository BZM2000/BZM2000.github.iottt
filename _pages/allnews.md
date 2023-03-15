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

<html>
    <head>
        <title>GPT-3.5 Turbo Model API Playground</title>
        <style>
            body {
                background-color: #E5E5E5;
                font-family: Arial, sans-serif;
            }

            #playground {
                width: 70%;
                margin: 0 auto;
            }

            .input-box {
                width: 100%;
                background-color: #F5F5F5;
                padding: 10px;
                border: 1px solid #D3D3D3;
            }

            .output-box {
                width: 100%;
                background-color: #F5F5F5;
                padding: 10px;
                border: 1px solid #D3D3D3;
            }
            
            .button-box {
                width: 100%;
                padding: 10px;
            }

            .button {
                background-color: #0085FF;
                color: white;
                padding: 8px 20px;
                margin: 8px;
                border: none;
                cursor: pointer;
            }

            .button:hover {
                background-color: #008FFF;
            }
        </style>
    </head>
    <body>
        <div id="playground">
            <h1>GPT-3.5 Turbo Model API Playground</h1>
            <p>This playground allows you to call the GPT-3.5 Turbo Model API to generate natural language responses to your input.</p>
            <div class="input-box">
                <h3>Input</h3>
                <textarea rows="4" cols="50" name="userInput" id="userInput"></textarea>
            </div>
            <div class="output-box">
                <h3>Output</h3>
                <textarea rows="4" cols="50" name="userOutput" id="userOutput" readonly></textarea>
            </div>
            <div class="button-box">
                <button class="button" onclick="callGPT3API()">Generate Response</button>
            </div>
        </div>
        <script>
            function callGPT3API() {
                // Get user input
                let userInput = document.getElementById("userInput").value;
                
                // Call GPT-3.5 Turbo Model API
                let xhr = new XMLHttpRequest();
                xhr.open("POST", "https://api.gpt3.5turbo.com/v1/generate");
                xhr.setRequestHeader("Content-Type", "application/json");
                xhr.onload = function() {
                    let response = JSON.parse(xhr.responseText);
                    if (xhr.status == 200) {
                        // Set output
                        document.getElementById("userOutput").value = response.response;
                    } else {
                        console.log("Error: " + xhr.status);
                    }
                }
                xhr.send(JSON.stringify({
                    "input": userInput
                }));
            }
        </script>
    </body>
</html>
