SIMPLE PDF READER FOR ANDROID  (Android 12 and newer)
=====================================================

WHAT IT DOES
  - Clean home screen: Open PDF, Image to PDF, and your recent files.
  - Open any PDF (from the app, from Files, Chrome downloads, WhatsApp, Gmail ... "Open with").
  - Smooth scrolling, pinch-to-zoom, double-tap zoom, page number bubble, fast scroller, Go to page.
  - Night mode, tap the page to hide/show the toolbar, remembers the page you stopped at.
  - Menu (the three dots, top right):
      Open PDF...                  Recent files > (your last opened file is at the top)
      Image to PDF...              make a new PDF from photos (JPG / PNG)
      Insert picture (JPG / PNG)... add a picture to the PDF you are reading
      Save / Save a copy...        Share / Print / Close file
  - Insert picture: choose a JPG or PNG, it appears on the page. DRAG it anywhere, pull the round corner (or
    pinch) to resize, tap an arrow  (top-left, top-right, bottom-left, bottom-right) to jump it into a corner,
    scroll the page behind it to choose which page, then tap Place. Use menu > Save to keep it.
    The original page content is not changed - the picture is added on top.
  - Free, no ads, no account. Files stay on your phone (the internet permission is only for PDF web links).

NOT INCLUDED (this is the "simple" reader): password-protected PDFs, text search, editing text.

HOW TO GET THE APP (APK)  -  choose ONE way
  A) No installation on your PC (recommended):
     1. Make a free account at github.com and create a new repository (private is fine).
     2. Upload ALL files and folders of this project (including the hidden ".github" folder).
     3. Open the repository's "Actions" tab > "Build APK" > "Run workflow".
     4. After about 5 minutes open the finished run and download "SimplePDFReader-APK" (a zip with app-debug.apk).
  B) With Android Studio (free, big download):
     1. Install Android Studio, choose File > Open and select this folder, wait for "Gradle sync".
     2. Menu Build > Build Bundle(s) / APK(s) > Build APK(s). The file appears in app/build/outputs/apk/debug/.

INSTALL ON THE PHONE
  Send app-debug.apk to the phone (WhatsApp, Drive, USB). Open it. If Android asks, allow
  "Install unknown apps" for that app (Settings > Apps > Special access > Install unknown apps).
  Works on Android 12, 13, 14, 15 and newer.

FOR GOOGLE PLAY / SELLING
  The debug APK is fine for your own phones and customers you send it to. For Google Play you need a signed
  release build: create a key once with   keytool -genkeypair -v -keystore my-release-key.jks -alias release
  -keyalg RSA -keysize 2048 -validity 10000   then create keystore.properties next to settings.gradle.kts:
        storeFile=my-release-key.jks
        storePassword=...      keyAlias=release      keyPassword=...
  and run   gradle :app:bundleRelease   (Play wants the .aab file). KEEP the .jks file and passwords safe forever.
  A Google Play developer account costs a one-time US$25.

HONEST NOTE
  This project was written and checked for mistakes with a Java compiler on a computer, but it could not be built
  or run on a real phone in the place where it was made. If the build shows an error, send me the error text and
  I will fix it quickly.
