
### n8n OpenAI-Compatible API

This project exposes your n8n workflows as an OpenAI-compatible API. It lets chat clients interact with your agents as selectable models.

#### How It Works

The system uses two endpoints. The `/models` endpoint lists your tagged workflows. The `/chat/completions` endpoint processes prompts, supporting both JSON and streaming text responses.

#### Usage

1.  Import this workflow's JSON into n8n.
2.  Add the tag `aimodel` to workflows you want to expose.
3.  Set your client's OpenAI Base URL to your n8n webhook URL.

This enables centralized management of your n8n agents from a single interface.

NOTE: We used 'cf-ray' in the header (from cloudflare session) as for the Stream and Completion response. Do not forget to edit it to your choice form of ID. For your case, you might pass the session ID from your client calling the /chat/completions endpoint and use it.

---

Made with ❤️ by the Lucidus Fortis team
