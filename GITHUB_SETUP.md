# GitHub Setup - 5 Minute Checklist

1. On GitHub, create a new repository named `fitflow-redesign`.
2. Do not initialize it with a README if you are pushing this prepared folder.
3. In a terminal opened inside this folder, run:

```bash
git init
git add .
git commit -m "Initial FitFlow redesign architecture and technology decisions"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/fitflow-redesign.git
git push -u origin main
```

4. Open repository Settings -> Branches / Rules and protect `main` if your account supports it.
5. Copy the final GitHub URL and replace the placeholder in Section 6.1 of the report before submission.
