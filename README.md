# Perplexity Force Native STT ReVanced Patch

A custom ReVanced patch for the Perplexity Android application that disables the third-party Soniox realtime transcription engine and forces the use of the native Google Speech-to-Text (STT) engine.

## 🚀 Usage with ReVanced Manager (Phone)

You can load this patch directly in your phone's **ReVanced Manager** by setting it as a custom source:

1. Open **ReVanced Manager** -> **Settings** -> **Sources**.
2. Change the sources configuration:
   * **Patches organization**: `dalapenko` *(replace with your GitHub/GitLab username)*
   * **Patches source** (or repository): `perplexity-repatch` *(replace with your repository name)*
3. Restart the ReVanced Manager app.
4. Go to the **Patcher** tab and select the **Perplexity** app (compatible with version 2.90.0). The custom patch will be fetched and loaded automatically from your releases.

---

## 🛠️ Build from Source

If you want to compile the patch (`.rvp` file) manually:

### 1. Configure GitHub Packages Credentials
Because ReVanced libraries are hosted on the GitHub Packages registry, Gradle requires authentication to resolve dependencies. Add your GitHub credentials to the `gradle.properties` file in the root of the project:

```properties
githubPackagesUsername=YOUR_GITHUB_USERNAME
githubPackagesPassword=YOUR_GITHUB_PERSONAL_ACCESS_TOKEN
```
*(Your Personal Access Token requires the `read:packages` scope).*

### 2. Compile the Patch
Run the Android build task to compile the Kotlin code and bundle it into an Android-compatible `.rvp` format:
```bash
./gradlew buildAndroid
```
The compiled patch will be generated at `patches/build/libs/patches-1.0.0.rvp`.
