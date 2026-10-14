# CloudStore — AWS S3 Simulator

A browser-based educational simulation of Amazon S3 for BCSE355L Cloud Architecture Design.

## Features
- Create and select buckets
- Upload, list, search, download, and delete objects
- Storage usage dashboard and object count
- Enhancement: object tagging (Academic, Personal, Important, Work) and tag filtering
- Sorting and dark mode
- File Risk Radar: explainable rule-based indicators using filename keywords, extensions, file size, tagging, and possible duplicates
- Responsive layout

## File Risk Radar limitation
Risk scores are simple educational heuristics. They do not inspect file contents, detect malware, or replace antivirus/security tools. A flagged file is not proof of a threat, and an unflagged file is not guaranteed safe.

## Important limitation
This is a simulation, not a connection to AWS. Bucket metadata is stored in browser `localStorage`; file blobs are stored in browser `IndexedDB`. Data is local to the browser/device and is not uploaded to AWS.

## Run locally
Open `index.html` in a modern browser. If browser storage is restricted, run a simple local server:
`python -m http.server 8000`
Then visit `http://localhost:8000`.

## Deploy using GitHub Pages
1. Create a GitHub repository named `cloudstore-s3-simulator`.
2. Upload `index.html` and this `README.md` to the repository root.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select `main` and `/(root)`, then Save.
6. Wait for the deployment link to appear. Test the link in a private/incognito window.
7. As the assignment specifies faculty approval before deployment, show the local working version to your faculty first if that requirement is still being enforced.

## 90-second demonstration
1. Explain that S3 stores objects inside buckets.
2. Create a bucket and upload two sample files.
3. Search for a filename and sort by size.
4. Tag one file as Academic and filter by that tag.
5. Download the file and delete another.
6. Show the storage usage cards.
7. Open File Risk Radar and upload examples such as `passwords.txt`, `setup.exe` (use a harmless dummy file), and a normal PDF to compare scores and reasons.
8. Explain the enhancement: risk indicators are transparent heuristic rules, not a malware scan.
9. State clearly that this is a browser-based simulation and not actual AWS infrastructure.
