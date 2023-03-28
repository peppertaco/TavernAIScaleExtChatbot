## Terrible modification version to use chatbotkit

Anyway it works


---
---
---
# Original readme

# TavernAI scale spellbook
quick hack to get tavernai to work with spellbook.scale.com for playing around with GPT4. based off of [cncanon1's](https://github.com/CncAnon1/) existing OpenAI mod.

### **Context size update (17 March 2023)** 
Now supports full GPT-4 8k context size.  Context size is limited to 7750 tokens in TavernAI to allow space for the system prompt.

## Quickstart
If you don't want to set up any of the shit below, you can just download it and run. It is preconfigured to connect to a bot.  Just launch `Start.bat` to get started.  Node.js v18 is required. 

⚠️ **Beware that if you do not change the API key, I can see your degenerate prompts and I WILL read your ERP.** ⚠️ 

If you want your own private (lol) bot, follow the guide below.

## Configuration
- Create scale spellbook account at https://spellbook.scale.com.
- Create an "App" (name/desc doesn't matter)
- Create a "Variant", which sets the parameters (system prompt, model, temperature, stop sequence, respnse token limit, etc) for your bot
- **Make sure to select GPT-4, you retard**
![https://i.imgur.com/ipmWkmu.png](https://i.imgur.com/ipmWkmu.png)
- Replace the contents of the "User" section of the prompt with the following:
```
Complete the next response in this fictional roleplay chat.

{{ input }}
```
- 💡 Set the model parameters as desired.
  - **Model:** GPT-4
  - **Temperature:** ~0.6 - 0.9
  - **Maximum Tokens:** 400 - 4096
    - This controls the max length of the AI's responses, NOT the context size. ***If you set this to a very high value, you MUST adjust the "Max Response Size" value in TavernAI's settings to match!***
    - I recommend 300 - 500 for chat purposes. You don't want the AI sending you 4000 token chat messages.
- Click "Save New Variant"
- Go to your new Variant and click Deploy
![https://i.imgur.com/5Tuj55L.png](https://i.imgur.com/5Tuj55L.png)
- This will create an API key and URL for your bot.
![https://i.imgur.com/eydf2XC.png](https://i.imgur.com/eydf2XC.png)
- Launch the server using the command line by running `.\Start.bat`.
- Open the TavernAI sidebar, switch the API to "Scale", and paste your API key and URL in the boxes. Click "Connect".
- Now start having fun with GPT4 :)
