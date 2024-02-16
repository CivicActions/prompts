This is used to manage bot and prompt configuration for CivicActions Slack chatbot.

All configuration is in the [config.yaml](config.yaml) file. There is a default configuration, then a configuration for additional bots that are available.

Each bot can include the following parameters, all optional:
* `description`: A message describing the bot behaviour. If this is a prompt created elsewhere include a link and license.
* `prompt`: Override a default or earlier prompt.
* `prompt_extra`: Extend a default or earlier prompt by adding this on the end. Generally preferred over `prompt` as this provides for additional flexibility in composing prompts.
* `temperature`: Set the temperature between 0 and 2 - the controls how much randomness is incorporated into the generative algorithm. Higher values tend to lead to more "creative" output.
* `max_tokens`: Cap the number of tokens to be output. Users can ask the bot to "continue" if more output is desired.

Users are able to compose multiple bots in order - e.g. `bot1+bot2` - each parameter overrides the default or earlier parameters, except for prompt_extra which will append to the previous prompt.

The following parameters are also available, but generally are only used in specific situations.
* `model`: The provider to use (needs to be preconfigured)
* `deployment`: The specific deployment at the provider to use (needs to be preconfigured)
