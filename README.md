# echo-bot
Steps to build an Echo Chat Bot using Microsoft Bot Framework SDK

## Introduction
Echo-Bot is a simple chat-bot which replies back whatever user inputs to it as text. Here, we will be building this bot using [Microsoft Bot Framework SDK](https://github.com/microsoft/botframework-sdk) which is used to develop conversational applications in Python, Java, JavaScript, C#. We will test this bot using the [Bot Framework Emulator](https://github.com/microsoft/BotFramework-Emulator) which is used to test/debug these bots locally or remote.

## Pre-requisites
- Python 3.X version: 
  + [Installation using Anaconda distribution](https://docs.anaconda.com/free/anaconda/#installation)
  + [Python Website](https://www.python.org/downloads/)
- [Bot Framework Emulator](https://github.com/microsoft/BotFramework-Emulator/releases)

## Steps to create the echo-bot
1. Start up the terminal of your choice like [Jupyter terminal](https://jupyter.org/)

2. Install the dependencies like [`botbuilder-core`](https://pypi.org/project/botbuilder-core/), [`asyncio`](https://pypi.org/project/asyncio/), [`aiohttp`](https://pypi.org/project/aiohttp/), [`cookiecutter`](https://pypi.org/project/cookiecutter/)
    ```
    pip install botbuilder-core asyncio aiohttp cookiecutter==1.7.0
    ```

3. Run the following command to download the [echo-bot](https://github.com/microsoft/BotBuilder-Samples/blob/main/samples/csharp_dotnetcore/01.console-echo/EchoBot.cs) template
    ```
    cookiecutter https://github.com/microsoft/BotBuilder-Samples/releases/download/Templates/echo.zip
    ```
    You'll be prompted to give a **bot_name** and **bot_description**. ![image](https://user-images.githubusercontent.com/66770875/235717632-88c135bc-8995-48e2-8517-36344e2e8018.png)

4. Analyse the downloaded `echo-bot` in the IDE of your choice. ![image](https://user-images.githubusercontent.com/66770875/235718071-9ae96755-d285-4616-9ce3-1ae16dbdf88d.png)

5. Change directories to `echo-bot`.
    ```
    cd echo-bot
    ```

6. Install the dependencies for the echo bot template.
    ```
    pip install -r requirements.txt
    ```

7. Run the chat-bot:
    ```
    python app.py
    ```
    If everything runs successfully, you should see the below message in the terminal:
    ![Screenshot 2023-05-01 223232](https://user-images.githubusercontent.com/66770875/235719469-33abce5f-421c-4407-9369-8fc005d3cb0b.png)

8. Open Bot in Bot Framework Emulator application and connect to `http://localhost:3978/api/messages` to test the echo of the chat-bot
![image](https://user-images.githubusercontent.com/66770875/235720640-b02da39c-57e4-4392-88ab-ea960e472eb0.png)

