# FloodVision AI website

Static website for the FloodVision image-segmentation project. The frontend is
hosted separately from the inference API; no dataset or model weights are
included in this repository.

## Deploy on Vercel

1. Import the `floodvision-web` GitHub repository into Vercel.
2. Select **Other** as the framework preset.
3. Leave the root directory as `./` and deploy. No build command is required.
4. Once the Render API is deployed, paste its `/predict` URL into the
   **Backend API URL** field on the website.

The API URL can also be supplied as a query parameter:
`https://your-site.vercel.app/?api=https%3A%2F%2Fyour-api.onrender.com%2Fpredict`

Set the API's `ALLOWED_ORIGINS` environment variable to the exact Vercel site
origin (for example, `https://your-site.vercel.app`) so browser requests are
allowed.

## Run locally

Serve this directory with any static HTTP server, for example:

```bash
python3 -m http.server 5500
```

Then open `http://127.0.0.1:5500` and enter the running API's `/predict` URL.
