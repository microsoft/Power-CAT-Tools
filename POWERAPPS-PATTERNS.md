# PowerApps Pattern Implementation Documentation

## 1. Asset Optimization (`patternCheckMediaFileSize`)
**Logic:**  
Checks for media files that exceed a defined size threshold (300KB) or if App Checker results have an `app-UnusedMediaResources` issue.

- **Pass Example:** All media files are under 300KB and no `app-UnusedMediaResources` issue present in App Checker results.
- **Fail Example:** Files like `background.png` and `icon.jpg` exceed 300KB, or App Checker results have an `app-UnusedMediaResources` issue.

## 2. Unused Media Resources (`patternCheckUnusedMediaResources`)
**Logic:**  
Checks if App Checker results have an `app-UnusedMediaResources` issue.

- **Pass Example:** No `app-UnusedMediaResources` issue present.
- **Fail Example:** App Checker results show an `app-UnusedMediaResources` issue.

## 3. App Settings Flags (`patternCheckAppSettings`)
**Logic:**  
Ensures all relevant app settings in `AppSettingsList` are enabled.

- **Current AppSettingsList:**  
  - `sharepointselectsenabled`
  - `enableupdateifdelegation`
  - `mobilenativerendering`
  - `keeprecentscreensloaded`

- **Pass Example:** All settings in `AppSettingsList` are enabled.
- **Fail Example:** Any of the app settings in `AppSettingsList` are disabled.

## 4. Accessibility (`patternCheckAppCheckerAccessibilityIssues`)
**Logic:**  
Flags any accessibility issues identified by App Checker.

- **Pass Example:** No accessibility issues found.
- **Fail Example:** Accessibility issues are present in App Checker results.

## 5. Formulas, Controls with Low/No Usage (`patternCheckUnusedElements`)
**Logic:**  
Detects unused variables; ensures no `app-UnusedVariables` issues are present.

- **Pass Example:** No `app-UnusedVariables` issues.
- **Fail Example:** `app-UnusedVariables` issues detected.

## 6. Inefficient Delay Loading (`patternCheckDelayLoading`)
**Logic:**  
Ensures no `app-InefficientDelayLoading` issues are present.

- **Pass Example:** No `app-InefficientDelayLoading` issues.
- **Fail Example:** `app-InefficientDelayLoading` issues detected.

## 7. Named Formulas (`patternCheckForNamedFormulas`)
**Logic:**  
Checks if global variables or collections are initialized but never updated.

- **Pass Example:** All global variables or collections are updated.
- **Fail Example:** Any global variable or collection is initialized but not updated.

## 8. UX Layout (`patternCheckForUxLayout`)
**Logic:**  
Ensures the root control of each screen is a container.

- **Pass Example:** Root control of all screens is a container.
- **Fail Example:** Root control of any screen is not a container.

## 9. Code Readability (`patternCheckForCodeReadability`)
**Logic:**  
Checks for code without comments exceeding 1000 characters or nested `If` functions.

- **Pass Example:** Code is under 1000 characters and no nested `If` statements exist.
- **Fail Example:** Code exceeds 1000 characters or contains nested `If` statements.

## 10. Nested API Calls (`patternCheckForNestedAPICalls`)
**Logic:**  
Detects nested API calls within `Filter`, `Search`, `ForAll`, `LookUp`, and `Patch` operations.

- **Pass Example:** No nested API calls detected.
- **Fail Example:** Nested API calls using external data sources are present.

## 11. Error Handling (`patternCheckForErrorHandling`)
**Logic:**  
Ensures `Patch` operations are wrapped with `IfError`/`IsError` functions.

- **Pass Example:** All `Patch` operations are wrapped in `IfError`/`IsError`.
- **Fail Example:** A `Patch` operation with external data source is not wrapped.

## 12. N+1 Database or API Requests (`patternCheckForNPlusOneQuery`)
**Logic:**  
Detects N+1 query issues in Gallery child controls using external data sources.

- **Pass Example:** No unnecessary server calls in Gallery child controls.
- **Fail Example:** Gallery child controls make excessive server requests.

## 13. Inefficient Data Retrieval (`patternCheckForInefficientDataRetrieval`)
**Logic:**  
Detects usage of `Filter`/`Search` on external data sources inside `First`/`Last`/`FirstN`/`LastN`.

- **Pass Example:** No such inefficient pattern detected.
- **Fail Example:** Use of `First(Filter(...))` or similar with external data sources.

## 14. Nested Filters (`patternCheckForNestedFilters`)
**Logic:**  
Detects nested `Filter`/`Search`/`LookUp` functions using external data sources.

- **Pass Example:** No nested functions using external data sources.
- **Fail Example:** Nested `Filter`/`Search`/`LookUp` functions detected.

## 15. Patch Formula Optimization (`patternCheckForPatchFormulaOptimization`)
**Logic:**  
Checks if `Patch` functions use `Filter`/`Search`/`LookUp` as the second parameter with external data sources.

- **Pass Example:** `Patch` functions do not use these as second parameters.
- **Fail Example:** `Patch` functions incorrectly use these as second parameters.
