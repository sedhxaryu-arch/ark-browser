# ARK Browser Website

A responsive dark landing page for the ARK Browser Windows installer.

## Files
- `index.html` — page content and download links
- `styles.css` — responsive styling
- `script.js` — mobile navigation and current year
- `assets/ark.ico` — your supplied ARK logo, used in the website and favicon

## Before publishing: connect your real installer

The download buttons currently use a placeholder URL:
`https://github.com/YOUR-USERNAME/ark-browser/releases/latest/download/ARK-Setup.exe`

Replace `YOUR-USERNAME` with your GitHub username and make sure your GitHub repository/release asset names match. If your installer has another name, either rename the release asset to `ARK-Setup.exe` or update both links in `index.html`.

## Free publishing option: GitHub Releases + Cloudflare Pages

1. Create a public GitHub repository named `ark-browser` (or use your chosen repository name).
2. On your computer, rename your installer to `ARK-Setup.exe` if appropriate. Do not change the file extension if it is not actually a Windows installer.
3. Open the repository on GitHub → **Releases** → **Draft a new release**.
4. Create a version tag such as `v1.0.0`, add release notes, attach `ARK-Setup.exe`, and publish the release.
5. Update the download URL in both places in `index.html` to match your username/repository/asset.
6. Test the release URL in a private/incognito browser window. It should download the installer without requiring a GitHub login.
7. Create a Cloudflare account and open **Workers & Pages** → **Create** → **Pages** (labels may vary).
8. Choose **Connect to Git** and authorize the repository containing these website files.
9. For a plain static HTML site, use no build command and set the output directory to the folder containing `index.html` (if the repository root contains it, use `/` or the root option offered by the dashboard).
10. Deploy. Cloudflare will give you a public `*.pages.dev` address.
11. Open the live URL on desktop and mobile, test all navigation links and click the download button.

## Important
- The page is a static website. The installer is hosted separately on GitHub Releases.
- Do not claim security/privacy capabilities the browser does not actually implement.
- Consider signing your Windows installer with a code-signing certificate and scanning releases before publishing. Windows SmartScreen may warn users about unsigned or low-reputation installers.
- Keep your repository and release asset names consistent with the URL in `index.html`.
