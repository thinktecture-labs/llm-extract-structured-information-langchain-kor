# Extract structured data from human input text with an LLM

A demo that illustrates how to use [Kor](https://eyurtsev.github.io/kor/) to fill in form fields from a user's request. This can be useful, for example, to define filter settings using natural language.

## Schema

The JSON schema for Kor is defined in the file `schema.json`. See also [Schema from JSON](https://eyurtsev.github.io/kor/schema_from_json.html).

## Client

The client frontend was created with [GPT Engineer](https://github.com/AntonOsika/gpt-engineer). The prompt for it is in the file `prompt`. The client can be started by opening the file `index.html` in a browser.

## Server

The server is a Python FastAPI that accepts a query via HTTP Post at `/query`. The result of the call is the parsed request. An example request is located in the file [requests.http](./server/samples/requests.http)

*NOTE*:
Make sure to provide the OpenAI API key in an environment variable called `OPENAI_API_KEY`.

The server can be started as follows:

```bash
python ./server/server.py
```
