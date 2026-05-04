# Import Instructions

Use these steps to publish this repository to GitHub.

## Option A — Upload Through GitHub Web Interface

1. Create a new public repository named `ciforus-public`.
2. Do not add a README if you are uploading this full package.
3. Upload all files and folders from this package.
4. Commit with the message:

```text
Initial public information hub
```

## Option B — Push With Git

From inside the `ciforus-public` folder:

```bash
git init
git add .
git commit -m "Initial public information hub"
git branch -M main
git remote add origin https://github.com/Ciforus/ciforus-public.git
git push -u origin main
```

If your GitHub username or repository URL is different, replace the remote URL.

## After Publishing

1. Pin `ciforus-public` on the Ciforus GitHub profile.
2. Replace placeholder links in `links.md`.
3. Upload the official whitepaper, litepaper, audit, and pitch deck files if you want local copies in the repository.
4. Keep Issues, Discussions, Wiki, and Projects disabled in early phase unless there is a clear moderation plan.
