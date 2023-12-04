<p align="center">
    <img align='left' src="https://github.com/Kourva/AwesomeChatGPTBot/assets/118578799/ef1cfefd-1e58-45d3-8a3a-fa9988a8322e" width=200 height=200/>
    <h2>Free Chat GPT Telegram Bot </h2>
  <p><i>Free ChatGPT-3.5 Telegram Bot with option to remenber chat history and pre-defined roles!</i></p>
  <p><i>Without any <b>API-key</b> from OpenAI and other stuff <b>+</b> Inline bot</i></p>
</p>
<br><br>

# ▋Change Log
It seems that server used for this chatGPT has some issues.<br>
Check out [Here](#common-issue-empty-api-responses) for more details

Here are the latest additions:<br>
**[Dec 01, 2023] Smarter Re-generate:** Uses smarter way to re-generate replied question.<br>
**[Dec 01, 2023] Settings command:** Added setting command to change bot response setting.<br>
**[Dec 01, 2023] Added titles.py:** To make main code more clear.<br>
**[Dec 01, 2023] Error handling:** Added more handlers and depp link handlers.<br> 
> **[Nov 13, 2023] PEP8 fixes:** Fixed some PEP8 issues.<br>
> **[Nov 13, 2023] Extra commands:** Added `help`, `features` and `chat` commands.<br>
> **[Nov 13, 2023] MarkdownV2:** Added converter to convert regular markdown to Markdown V2.<br>
> **[Nov 13, 2023] History management**: Added utilities to check history and fix it when it got broken.<br>
> **[Nov 13, 2023] Re-Generate**: Users can re-generate their prompts, new answer will be raplaced with old one<br>
> **[Nov 13, 2023] Improved chat handler**: Users now requied to use /chat in groups to chat with bot.<bt>
```
/chat hi
```
> This will avoid mess in replies and even reactions to bot's responses

<br>

# ▋Upcoming Features
1. **Smart reply**: Reply to user's message to process them with GPT.<br>
2. **Code Generator**: Use code generator to generate functions in many languages.<br>
3. **Image generator**: Use AI to generate images from prompt.

<br>

# ▋Old Changes
> + history section added
> + **/history** to get history file in json format
> + **/reset** to reset the chat history
> + **/danmode** to enable/disable DAN mode v10.0 in bot
> Note: History will reset when using /danmode command!!

<br>

# ▋Bot is Down? Not working?
Visit https://status.fakeopen.com for more information about external API

<br>

# ▋Common Issue: Empty API Responses
### Problem Description
The problem often arises when the API doesn't return the expected data (empty string), affecting the functionality of the chat bot. I used error handler to handle this empty result and send `Error! ChatGPT is not responding at this time!` to the user instead of raising error from Telegram! <br>
This issue is caused by problems with the external API (Maybe IP limitation or bot chanllenges).
This is latest response from bot:
```json
{
    "error": {
        "message": "It is recommended to upgrade to the latest PandoraNext: https://github.com/pandora-next/deploy",
        "type": "invalid_request_error",
        "param": null,
        "code": null
    }
}
```
I'll wait for problem to solve and if not, I will change the request endpoints and find new one.

### Solutions
For now, simple solution is to resend your prompt and ask your question again.
+ [Nov 13, 2023]: Not fixed but you can re-generate your prompt with inline button.

### Contributions
I welcome contributions. If you've found a reliable solution to this issue or have other useful suggestions, please consider contributing to this project.

<br>

# ▋Features
This bot responds to every message with ChatGPT AI, excluding commands.
+ Inline mode for obtaining predefined roles. [**How to use**](https://github.com/Kourva/AwesomeChatGPTBot/issues/3#issuecomment-1791705893)
+ The ability to remember chat history (long-term memory).

<br>

# ▋Clone Repository
To get started, first you need to **clone** this repository from github into your machine:
```bash
git clone https://github.com/Kourva/AwesomeChatGPTBot
```
and if you dont have git you can install it from your package manager!

<br>

# ▋Install Requirements
Then you have to install requirements before running bot
1. Navigate to bot directory
2. Install requirements using pip
```bash
cd AwesomeChatGPTBot
```
```bash
pip install -r requirements.txt
```
This will install **pyTelegamBotAPI** and **Requests** for you

<br>

# ▋Configure your token
Now you have to get create bot from [BotFather](https://t.me/BotFather) **(If you don't have)** and take your **Token** to starts working with your bot.<br>
After getting **Token** from **BotFather** replace the Token in `utils.py` in line **7** as follows:
```python
# Bot token to use
Token = "6146793572:AAE7fbH29UPOKzlHlp0YDr9o06o_NdD4DBk"
```
> This is just an example Token. Use yours instead

<br>

# ▋Configure the bot commands (Optional)
you can set your bot's commands manually or using 'init.py' script
```bash
python init.py
```
> This will set up these commands in bot's menu
> + `/start`
> + `/help`
> + `/setting`
> + `/chat`
> + `/features`
> + `/history`
> + `/reset`
> + `/danmode`

<br>

# ▋Launch the bot
Now you are ready to launch your bot in polling mode inside your terminal using python
```bash
python main.py
```
You can also use **proxychains** to run your bot via **Tor** proxy
```bash
proxycahins python main.py
```
Or in quiet mode
```bash
proxychains -q python main.py
```
To install proxychains install `proxychains-ng` and then edit the config file in `/etc/proxychains.conf`.<br>
In config file comment the `strict_chain` and un-comment `dynamic_chain` and its ready to use.
<br>

# ▋TOR new IP address
If you got any denied requests that blocked your Ip address, you can renew your IP
```bash
sudo killall -HUP tor
```

<br>

# ▋Bot Inline Mode
Don't forget to enable **Inline Mode** in your bot.<br>
See documentation here: https://core.telegram.org/bots/api#inline-mode

<br>

# ▋Thanks a bunch for starring the project! :star:
If you have any suggestions or feedback, feel free to share. I appreciate your interest and contribution to the project!

<picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=kourva/AwesomeChatGPTBot&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=kourva/AwesomeChatGPTBot&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=kourva/AwesomeChatGPTBot&type=Date" />
</picture>


