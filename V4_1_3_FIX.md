# V4.1.3 Fix

Build error fixed in:
`app/src/main/java/com/traveler/schedule/widget/TravelerWidgetUtils.kt`

Cause:
The widget utility referenced `MainActivity::class.java` directly, but GitHub Actions could not resolve `MainActivity` while compiling the widget source.

Fix:
- Removed `import com.traveler.schedule.MainActivity`
- Replaced direct class reference with explicit Android component class name:
  `Intent().setClassName(context, "com.traveler.schedule.MainActivity")`
- This keeps widget navigation behavior while removing the Kotlin compile-time dependency.

Version:
- versionCode = 19
- versionName = 4.1.3
