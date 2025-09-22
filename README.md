### Overview MySum - Storage Management App
An Android-based storage management application for organization secretariats. Users can view available items, their quantities, borrow and return items, all within one app. Data is stored and synchronized using Firebase.

### 🚀 Features
- **Storage List**: Displays all available items along with their quantities.
- **Checkout List**: Shows the list of items selected for borrowing.
- **Borrowing Form**: A form to submit borrowing requests.
- **Calendar** :Allows users to track borrowing dates and return deadlines.
- **Ongoing, Pending, History**: Sections to monitor borrowing activities based on their status.

### 📁 File Structure
```text
MySUM/
  app/
    build.gradle.kts
    google-services.json
    proguard-rules.pro
    src/
      main/
        AndroidManifest.xml
        java/com/...        # Kotlin sources
        res/
          drawable/         # Vector drawables and shapes
          layout/           # XML layouts (supports view/data binding)
          menu/             # App menus
          mipmap-*/         # App icons
          values/           # Colors, strings, themes
          xml/              # Misc XML (e.g., filepaths, network config)
  build.gradle.kts          # Gradle build
  gradle/
    libs.versions.toml      # Version catalog
    wrapper/                # Gradle wrapper
  gradle.properties
  settings.gradle.kts
  local.properties          # SDK path
```

### ⚙️ Setup & Configuration
1. **Prerequisites**
   - Android Studio (Giraffe/Koala or newer)
   - JDK 17 (bundled with recent Android Studio)
   - Android SDK + Build Tools (install via SDK Manager)
2. **Open the project**
   - Open the `MySUM` folder in Android Studio and let Gradle sync.
3. **Firebase (optional)**
   - Ensure `app/google-services.json` matches your Firebase project and package name.
   - Re-sync Gradle after adding the file.
4. **Run**
   - Select a device/emulator and click Run.

### 🔧 Advanced Configuration
- **Signing configs**: Add release keystore in `app/build.gradle.kts`; keep secrets in `gradle.properties` or CI.
- **Build types & R8/ProGuard**: Customize rules in `app/proguard-rules.pro`.
- **Local settings**: `local.properties` should contain `sdk.dir=...` and is not committed.
- **User/app config**: Adjust `app/user.json` usage as needed for runtime configuration.

### 🎯 How It Works
- 1. Users register and log in.
- 2. Browse and view items available in storage.
- 3. Add items to the checkout cart.
- 4. Fill out the borrowing form.
- 5. Regularly check the calendar to see borrowing and returning schedules.

### 🐛 Troubleshooting
- **Gradle sync fails**: Check internet, Gradle and JDK versions; try File → Invalidate Caches / Restart.
- **SDK not found**: Ensure `local.properties` contains a valid `sdk.dir` path.
- **Duplicate classes/conflicts**: Inspect the dependency graph and align versions in `libs.versions.toml`.
- **Firebase errors**: Verify `applicationId` matches the `package_name` in `google-services.json`.
- **Build issues**: Clean and Rebuild the project; delete `.gradle`/`build` directories if needed and re-sync.

### 📞 Support
- Open an issue in your repository or contact the maintainer.
- For internal projects, use your team’s support channel.
