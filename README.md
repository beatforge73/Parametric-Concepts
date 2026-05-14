# Parametric Concepts — Website Template

## What's in here

```
site/
├── index.html      ← Main page (project info, news)
├── release.html    ← Album page (tracklist, audio players, downloads)
├── links.html      ← Links, credits, contact
├── style.css       ← All the styling (one file, easy to tweak)
├── images/         ← Put your photos here
│   ├── project-photo.jpg
│   └── album-cover.jpg
└── audio/          ← Put your music files here
    ├── 01-track-title.mp3   (for streaming on the page)
    ├── 01-track-title.wav   (for downloads)
    └── ...etc
```


## How to edit

1. Open any .html file in a text editor (Notepad, TextEdit, or VS Code)
2. Find the HTML comments like <!-- WRITE YOUR TEXT HERE -->
3. Replace placeholder text with your own words
4. Save the file
5. Open it in a browser to see how it looks

You don't need to learn HTML — just change the text between the tags.
If you break something, the comments help you find where things go.


## Audio setup

For each track you need TWO files:
- An .mp3 file (for the in-browser audio player — 320kbps recommended)
- A .wav file (for the download link)

Name them consistently:
  01-track-name.mp3
  01-track-name.wav

The audio player uses `preload="none"` so the page loads fast — 
tracks only start loading when someone presses play.

To offer a full album download, zip all .wav files into one .zip
and put it in the audio/ folder.


## How to get it online (GitHub Pages)

### First time setup

1. Create a GitHub account at https://github.com
2. Click the "+" in the top right → "New repository"
3. Name it: parametric-concepts (or whatever you like)
4. Make sure "Public" is selected
5. Click "Create repository"
6. On the repository page, click "Add file" → "Upload files"
7. Drag in ALL your files: the .html files, style.css, 
   and the images/ and audio/ folders with your content
8. Write a short commit message (e.g. "first upload") and click "Commit"
9. Go to Settings → Pages (in the left sidebar)
10. Under "Source", select: Branch = main, Folder = / (root)
11. Click Save

Your site will be live within a couple of minutes at:
  https://YOUR-USERNAME.github.io/parametric-concepts/


### Adding a custom domain

Once you've registered a domain (e.g. at Domeneshop or Namecheap):

1. In your GitHub repo: Settings → Pages → Custom domain
   Type your domain (e.g. parametricconcepts.com) and save.
   This automatically creates a CNAME file in your repo.

2. At your domain registrar, add these DNS records:

   A records (point the root domain to GitHub):
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153

   CNAME record (for the www version):
     www → YOUR-USERNAME.github.io

3. Back in GitHub Pages settings, check "Enforce HTTPS"
   (may take a few minutes to become available)

4. Done. Your site is live at your domain with free HTTPS.


### Updating the site later

To change anything after the initial upload:
1. Go to your repository on github.com
2. Click on the file you want to change
3. Click the pencil icon to edit (for HTML/CSS)
   — or use "Add file" → "Upload files" for new images/audio
4. Commit the changes
5. The site updates automatically within a minute or two


## Storage and limits

GitHub Pages allows:
- 1 GB total per repository (soft limit)
- 100 MB per individual file
- 100 GB bandwidth per month (more than enough)

Your estimated usage:
  7 tracks × ~50 MB (.wav) = ~350 MB
  7 tracks × ~10 MB (.mp3) = ~70 MB
  A couple of images         = ~5 MB
  Total: ~425 MB — fits comfortably

Note: if any single .wav file is over 100 MB (very long tracks),
you'd need to use Git LFS or compress to FLAC instead.


## Customizing the look

Open style.css and change:
- background-color: #e8e0d4  → change the page color
- color: #1a1a1a             → change the text color
- font-family                → change the font
- Any colors, sizes, spacing you want

The current look: warm beige background, serif body text, 
monospace headings. Deliberately plain, like a real handmade site.
