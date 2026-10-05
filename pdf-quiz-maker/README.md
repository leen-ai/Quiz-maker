# PDF Quiz Maker

Upload a PDF of your notes or slides and get multiple-choice questions you can answer and check instantly. Questions are written by Google Gemini using a free API key.

Everything runs in the browser. There is no server: the PDF is read on your device, and only its text is sent to Google to write the questions.

## Use it

1. Get a free Gemini API key: go to https://aistudio.google.com/apikey, sign in with your Google account, and click **Create API key**. No credit card is needed.
2. Open the site, paste your key, and click **Connect**.
3. Choose a PDF, pick the number of questions and the difficulty, then click **Generate quiz**.
4. Click an answer to see if it's right, with a short explanation. Your score is shown at the top.

Scanned PDFs (pictures of pages) can't be read. PDFs saved from Word or PowerPoint work best.

## Put it on GitHub Pages

1. Create a new public repository on GitHub, for example `pdf-quiz-maker`.
2. Upload `index.html` and `README.md` (Add file > Upload files), then commit.
3. Go to **Settings > Pages**. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
4. After a minute your site is live at `https://<your-username>.github.io/pdf-quiz-maker/`. Share that link.

## Built-in key (so nobody has to type one)

1. Open `index.html` in a text editor (Notepad or VS Code).
2. Find `const BUILT_IN_KEY = "";` near the top of the `<script>` and paste your key between the quotes, for example `const BUILT_IN_KEY = "AIza...";`. Save.
3. **Restrict the key before you upload it.** The page is public, so anyone can view the code and copy the key. Go to https://console.cloud.google.com/apis/credentials, open your key, and set:
   - **Application restrictions:** Websites, and add `https://<your-username>.github.io/*`
   - **API restrictions:** Restrict key, and pick only **Generative Language API**
   Save. Now the key only works from your site.
4. Upload the new `index.html` to GitHub.

Everyone who uses your site shares your free limit. When it runs out, a yellow notice appears at the top of the page saying when it resets, and people can paste their own key instead. If someone misuses your key, delete it in AI Studio and make a new one.

Tip: if you only want to skip typing the key yourself, you don't need any of this. Paste your key once and tick **Remember my key in this browser**.

## Good to know

- The free tier has per-minute and daily limits. Daily limits reset at midnight Pacific time (3:00 or 4:00 PM in the Philippines). The notice at the top shows the exact time.
- On the free tier, Google may use what you send to improve its products, so avoid uploading private documents.
- "Remember my key" saves it only in that person's browser. Leave it unticked on shared computers.
