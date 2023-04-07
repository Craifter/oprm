# oprm Format

## What is it?

A file format for AI prompts, designed to efficiently store and organize prompts and their corresponding template strings. This format is based on a widely used and easy-to-parse format like JSON. Let's call this format "Open Prompt" (OPRM).

## File Format

```
{
    "version": "0.0.1",
    "generator": "ChatCrafter",
    "prompts": [
        {
            "id": "name-generator",
            "name": "name generator",
            "description": "Gives names for a gender",
            "prompt": "Give me names for a {{gender}}",
            "variables": [
                {
                    "name": "gender",
                    "type": "string",
                    "description": "Girl or Boy"
                }
            ],
            "tags": ["person", "names"],
            "metadata": {
                "author": "Jane Doe",
                "creation_date": "2023-04-05",
                "source": "https://www.example.com/ai-promt"
            },
            "model": {
                "id": "gpt-3.5-turbo",
                "name": "GPT-3.5",
                "maxLength": 12000,
                "tokenLimit": 4000
            }
        }
    ]
}
```

## Promt Syntax

| Variable    | Type   | Description                                           |
| ----------- | ------ | ----------------------------------------------------- |
| id          | string | Identifier for this prompt                            |
| name        | string | Name of this promt                                    |
| description | string | Describe what this promt does                         |
| promt       | string | The actual promt with variables inside, like {{name}} |
| variables   | object | List of possible variables                            |
| tags        | array  | List of tags fitting to the promt                     |
| metadata    | object | Additional information                                |
| model       | object | Information about the model for which the promt is    |
