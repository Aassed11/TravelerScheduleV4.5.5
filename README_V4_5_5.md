# TRAVELER Schedule V4.5.5 — Build Fix

GitHub Actions V4.5.4 compiler errors fixed.

Root cause:
- `verticalScroll` was used without importing `androidx.compose.foundation.verticalScroll`.
- `LazyRow` was used without importing `androidx.compose.foundation.lazy.LazyRow`.
- The remaining errors around `items`, `it`, `country`, and composable invocation were cascading errors caused by the missing `LazyRow` import.

Fix:
- Added `import androidx.compose.foundation.verticalScroll`
- Added `import androidx.compose.foundation.lazy.LazyRow`

Version:
- versionCode 30
- versionName 4.5.5
