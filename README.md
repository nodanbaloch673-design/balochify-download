# Balochify download site

This is a separate, static GitHub Pages site. It does not contain or expose the Android app source code. The APK download button points to the latest GitHub Release asset in a public `balochify-download-site` repository.

## Before publishing

1. Replace `YOUR_GITHUB_USERNAME` in `index.html` with your GitHub username.
2. No contact address is shown yet. Add one only if you want visitors to contact you.
3. Wait until a signed APK is ready. The current Android project is a prototype with no verified dictionary entries yet.

## Publish the site and APK from a separate repository

1. On GitHub, create a **new public repository** named `balochify-download-site`.
2. Upload `index.html` and the `assets` folder from this directory to the repository's root. Do not upload the Android project or its signing key to this public repository.
3. In the repository, open **Settings → Pages**. Under the build/deployment source, select **Deploy from a branch**, branch `main`, folder `/ (root)`, and click **Save**.
4. When the signed APK is ready, open **Releases → Create a new release** in this same repository. Use a tag such as `v1.0.0`, attach the APK with the exact filename `Balochify.apk`, and publish the release.
5. The page will be available at `https://YOUR_GITHUB_USERNAME.github.io/balochify-download-site/`. The button downloads `https://github.com/YOUR_GITHUB_USERNAME/balochify-download-site/releases/latest/download/Balochify.apk`.

GitHub Pages on the free plan requires a public repository. The APK release asset will also be public, so anyone with the page or release link can download it.

## Safety and updates

- Keep the Android signing keystore and its passwords private and backed up. Never commit them to GitHub.
- Sign each update with the same Android signing key so users can install it over the earlier version.
- Change the release tag and app version for every new release, while keeping the APK asset filename `Balochify.apk` so the latest-download URL continues to work.
- Tell users to install only the APK linked from this official page. Android may ask them to allow installs from their browser.
