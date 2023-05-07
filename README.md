# openplayground

An LLM playground you can run on your laptop.

https://user-images.githubusercontent.com/111631/227399583-39b23f48-9823-4571-a906-985dbe282b20.mp4

#### Features

- Use any model from [OpenAI](), [Anthropic](), [Cohere](), [Forefront](), [HuggingFace](), [Aleph Alpha](), and [llama.cpp]().
- Full playground UI, including history, parameter tuning, keyboard shortcuts, and logprops.
- Compare models side-by-side with the same prompt, individually tune model parameters, and retry with different parameters.
- Automatically detects local models in your HuggingFace cache, and lets you install new ones.
- Works OK on your phone.
- Probably won't kill everyone.


#### Note: THIS IS A TRUNCATED README FOCUSED SUPPORTING A LOCAL INSTANCE WITH GPT-LLAMA.CPP, TO SEE FULL README PLEASE SEE [THE ORIGINAL REPO](https://github.com/nat/openplayground)
## How to run for development

```sh
git clone https://github.com/keldenl/openplayground # or git@github.com:keldenl/openplayground.git for SSH
cd app && npm install # Install requirements
npx parcel watch src/index.html --no-cache # Run the front end

# Open another terminal / cmd window
cd server && pip3 install -r requirements.txt && cd .. # Install requirements
python3 -m server.app # Run the backend
```


### gpt-llama.cpp
To run openai requests through gpt-llama.cpp, please make sure you have a server instance of `gpt-llama.cpp` running. If not, please follow this [separate guide](https://github.com/keldenl/gpt-llama.cpp#quickstart-installation).

Run openplayground as specified above, and when setting the API KEY remember to set it as the path to your local model. Set the custom base url to `http://localhost:443/v1`, replace "443" with the port you are using.

`gpt-3.5-turbo` will produce results in "chat completion" style, while models like `text-davinci-003` will produce results as "text completion" style.

#### Credits

Instigated by Nat Friedman. Initial implementation by [Zain Huda](https://github.com/zainhuda) as a repl.it bounty. Many features and extensive refactoring by Alex Lourenco.
