# Bangla Caption Studio — releases

Signed `.zxp` builds of **Bangla Caption Studio**, a Premiere Pro panel that makes Bangla captions from your sequence audio. The panel checks this repo for new versions.

## Install on a new PC

1. Download the latest **`BanglaCaptionStudio-x.y.z.zxp`** from [Releases → Latest](https://github.com/dothack009/bangla-caption-studio-releases/releases/latest).
2. Install it with **[ZXP Installer](https://aescripts.com/learn/zxp-installer/)** (free, Mac & Windows). Drag the `.zxp` onto the app.
3. Restart Premiere Pro, then open **Window → Extensions → Bangla Caption Studio**.
4. In Premiere: **Settings → Graphics → Text Engine → South Asian and Middle Eastern**, then restart Premiere (needed for correct Bangla letters).
5. In the panel's ⚙ Settings, paste a free API key (Gemini: aistudio.google.com/apikey, or Groq: console.groq.com/keys).

## Updates

The panel checks for new releases when it opens. When one is available it shows **"Update x.y.z available → Install"**. Click Install, then Restart. If the panel was installed for all users, your Mac asks for your admin password.

You can also check by hand in **⚙ Settings → Updates → Check for updates**.

## If the panel opens blank

This is Adobe's [known ZXP signing issue](https://github.com/Adobe-CEP/CEP-Resources/blob/master/ZXPSignCMD/KnownIssue2024.md). Turn on CEP debug mode once, then restart Premiere Pro:

- **Mac** (Terminal): `for v in 9 10 11 12 13 14; do defaults write com.adobe.CSXS.$v PlayerDebugMode 1; done`
- **Windows** (Command Prompt): `for %v in (9 10 11 12 13 14) do reg add "HKCU\Software\Adobe\CSXS.%v" /v PlayerDebugMode /t REG_SZ /d 1 /f`
