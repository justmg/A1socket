# Twilio Realtime WebSocket Server

WebSocket server for the Twilio Realtime API demo using OpenAI's Realtime API.

## Features

- WebSocket server handling Twilio phone calls
- Integration with OpenAI Realtime API
- Function calling support
- TwiML response generation
- Health check endpoint for Railway deployment

## Environment Variables

- `OPENAI_API_KEY`: Your OpenAI API key
- `PUBLIC_URL`: Your deployed server URL (set by Railway)
- `PORT`: Server port (set by Railway)

## Deployment

This server is designed to be deployed on Railway.

### Railway Deployment

1. Connect this repository to Railway
2. Set environment variables:
   - `OPENAI_API_KEY`: Your OpenAI API key
3. Railway will automatically set `PUBLIC_URL` and `PORT`

## Local Development

```bash
npm install
cp .env.example .env
# Add your OpenAI API key to .env
npm run dev
```

## API Endpoints

- `GET /health` - Health check endpoint
- `GET /public-url` - Returns the public URL
- `POST /twiml` - Returns TwiML for Twilio
- `GET /tools` - Returns available function schemas
- `WS /call` - WebSocket endpoint for Twilio calls
- `WS /logs` - WebSocket endpoint for frontend logging