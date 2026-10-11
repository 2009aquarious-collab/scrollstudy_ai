SCROLLSTUDY AI — EASY SETUP

WHAT THIS ADDS
- The Create a Lesson button calls OpenAI through a Netlify serverless function.
- AI creates short lesson slides and a multiple-choice quiz based on the notes.
- Your OpenAI API key stays server-side in Netlify; it is not placed in index.html.

IMPORTANT
This is an AI lesson/quiz generator, not an AI-rendered video or voice narration generator. The site still uses your existing Supabase configuration for sign-in/data. Confirm that the Supabase project URL and public/publishable key in index.html are for the current project before deploying. Never place a Supabase service-role/secret key in index.html.

DEPLOYMENT NOTE
Netlify Functions require a deploy method that processes the netlify/functions folder (for example, connecting a Git repository to Netlify, or deploying with Netlify CLI). Uploading only index.html or a plain drag-and-drop static deploy will not deploy the function.

FILES
- index.html: updated website
- netlify/functions/generate.js: secure AI server function
- netlify.toml: tells Netlify where the site and function live

NEXT STEPS
1. Put these files in a GitHub repository (the contents of this folder, not the ZIP itself).
2. Connect that repository to your existing Netlify site so Netlify builds/deploys it.
3. In Netlify site environment variables, set OPENAI_API_KEY to your private OpenAI API key. Do not share the key in chat.
4. Trigger a new deploy after adding the variable.
5. Test Create a lesson using non-sensitive notes. API usage may cost money and may require API billing.

This package does not include any secret API key.
