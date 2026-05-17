<details>
<summary>🌍 Language Localizations</summary>

<br>

<div align="center">

Simple internationalization setup for Flutter using **flutter_localizations** and **intl**.

</div>

---

## 📦 Install Packages

Run the following commands in your terminal:

```bash
flutter pub add flutter_localizations --sdk=flutter
flutter pub add intl:any
```

---

## ⚙️ Enable Code Generation

Inside your `pubspec.yaml` file, enable generation under the `flutter:` section:

```yaml
flutter:
  uses-material-design: true
  generate: true
```

---

## 🗂️ Create `l10n.yaml`

Create an `l10n.yaml` file in the **project root** and paste the following:

```yaml
arb-dir: lib/l10n
template-arb-file: app_en.arb
output-localization-file: app_localizations.dart
```

Then run the following command in the terminal:

```bash
flutter pub get
```

> This will automatically generate the `app_localizations.dart` file in your project.

---

## 🔌 Integrate Into `main.dart`

After importing `app_localizations.dart` into your `main.dart`, add the localization delegates and supported locales:

```dart
return MaterialApp(
  title: 'Flutter Demo',
  theme: AppTheme.lightTheme,
  darkTheme: AppTheme.darkTheme,
  themeMode: ThemeMode.system,
  home: const MyHomePage(title: 'Flutter Demo Home Page'),
  localizationsDelegates: AppLocalizations.localizationsDelegates,
  supportedLocales: AppLocalizations.supportedLocales,
);
```

---

<div align="center">

✅ **Your Flutter localization setup is now ready.**

</div>

</details>

<details>
<summary>🎨 Light / Dark Theme</summary>

<br>

After importing the `AppTheme` file into `main.dart`, set the `theme`, `darkTheme`, and `themeMode` parameters as shown below:

```dart
return MaterialApp(
  title: 'Flutter Demo',
  theme: AppTheme.lightTheme,
  darkTheme: AppTheme.darkTheme,
  themeMode: ThemeMode.system,
  home: const MyHomePage(title: 'Flutter Demo Home Page'),
  localizationsDelegates: AppLocalizations.localizationsDelegates,
  supportedLocales: AppLocalizations.supportedLocales,
);
```

> Using `ThemeMode.system` means the app automatically switches between light and dark based on the device's system setting.

</details>
