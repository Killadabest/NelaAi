# Nela AI

A minimalist chat interface with a rotating 3D sphere (Jarvis-style) and text-to-speech.

**Built by Claude for the Lovable community.**

## Features

- **3D Rotating Sphere** — powered by Three.js, with Jarvis-like ambient pulse
- **Auto-fetched API Key** — pulled from a secure paste endpoint, not hardcoded
- **Gemini 3 Flash Preview** — latest Google AI model
- **Text-to-Speech** — toggle with the speaker button in the chat input
- **Clean Chat-Only Layout** — no nav, no hero, just conversation

## Files

- `index.html` — minimal HTML structure
- `style.css` — dark theme styling
- `script.js` — chat logic, 3D sphere init, TTS

## How it works

1. On load, the page fetches your Gemini API key from a public paste endpoint:
   ```
   https://paste-api-sync.lovable.app/api/public/bc4704b6a6
   ```
   (Update the `API_KEY_ENDPOINT` constant in `script.js` if you want a different key)

2. Start typing and press Enter or click Send.

3. Toggle TTS (speaker icon) to hear bot replies read aloud.

4. The 3D sphere rotates continuously in the background.

## Deployment

Push to GitHub and enable Pages on the `main` branch. No build step needed.

## Customization

- **Model**: change `MODEL` in `script.js` (currently `gemini-3-flash-preview`)
- **System prompt**: edit `SYSTEM_INSTRUCTION` in `script.js`
- **Colors**: edit CSS variables in `style.css` (`:root`)
- **Sphere color/speed**: adjust Three.js material and rotation in `initSphere()` function

## API Key Security

The key is fetched from a public paste endpoint at runtime — it's never stored in the repo. The endpoint returns plain text, cached in the browser for the session. No authentication is needed.

## License

MIT
