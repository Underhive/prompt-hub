# prompt-hub
A library of "open-source" prompts.

## Why?
It's clear that LLMs are providing a lot of value already as they act as a new tool people can use to get work done. Almost like how people can use programming languages to engineer behaviours into machines.

I'm not sure where I personally would be as an engineer if I didn't have access to github and all the open source repositories that there are in the world to learn from.
We can't close-source every single thing we create, we need to put out things in open so people can learn from them and create.

We're creating this repository of prompts which can maybe help people just stepping into the world of LLMs.

## Mongo Collection
All the data that you see in `hub.json` is also synced with a public (read-only) mongodb collection.
```nodejs
mongodb+srv://prompts-reader:Xa9wOlOzFz0U5OjE@underhive.0f84b.mongodb.net/
```

## Schema 
It's a list of json objects and each object is supposed to define a single prompt (system prompt + input prompt)
```js
{
  "category": "", // name the category as you see fit
  "task": "", // sub-category of the task that this particular prompt is supposed to help with
  "about": "", // a short description for the prompt
  "system_prompt": "",
  "input": "", // input prompt for the task, you can add parameters for the dynamic input prompts. parameter names should be surrounded with double braces '{{ }}'.
  "input_variables": [], // list of names of input prompt's variables if any. default []
  "output": "", // example output
  "input_format": "",
  "output_format": "", // output type declaration. eg: natural_language, json, markdown, html, python, javascript, stateless_prompt, stateful_prompt, etc.
  "input_schema": {}, 
  "output_schema": {}, 
  "source": "", // a source url declaring the author of the prompt
  "tags": [] // relevant tags for the prompt
}

```

## Contribution guidelines
As long as you can add prompts following the above schema, you're welcome to contribute.
Please don't edit other people's prompts you can just create a new version of the prompt if you need to.

## Future
We'll soon launch a public service where people can create their own repositories of prompts. 
It'll be free ofcourse.
