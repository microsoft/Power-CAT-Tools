# PowerAutomate Pattern Implementation Documentation

## 1. Unused Variables (`patternCheckUnusedVariables`)
**Logic:**  
Checks for unused variables in Power Automate flow. These variables can be removed.

- **Pass Example:** All declared variables are referenced at least once.
- **Fail Example:** Variable `varHasNextStage` is declared but never referenced.

## 2. Static Variables (`patternCheckStaticVariables`)
**Logic:**  
Checks for variables initialized but never updated. Such variables can be replaced with Compose actions.

- **Pass Example:** Variable `isApproved` is declared, initialized, and updated using Set Variable action.
- **Fail Example:** Variable `isApproved` is declared and used but never updated.

## 3. Multiple Initialize Variable Actions (`patternCheckMultipleInitializeVariable`)
**Logic:**  
Counts initialize variable actions. If more than one, the pattern fails. Prefer a single object variable.

- **Pass Example:** Flow with zero or one initialize variable action.
- **Fail Example:** Flow with more than one initialize variable action.

## 4. Scope Usage (`patternCheckScopeUsage`)
**Logic:**  
Checks if flows with more than 10 actions contain a Scope action.

- **Pass Example:** Flow with 15 actions and Scope action present.
- **Fail Example:** Flow with 15 actions and no Scope action.

## 5. Data Retrieval Parameters (`patternCheckDataRetrievalParameters`)
**Logic:**  
Ensures filter, top, and select parameters are used in Dataverse and SharePoint data actions.

- **Dataverse List Rows:**
  - **Pass Example:** All three (filter, select, top) parameters are used.
  - **Fail Example:** Any parameter (filter, select, or top) is empty.

- **Dataverse Get a Row By ID:**
  - **Pass Example:** Select parameter used to retrieve only relevant columns.
  - **Fail Example:** Select parameter missing.

- **SharePoint Get Items:**
  - **Pass Example:** Both filter and top parameters are used.
  - **Fail Example:** Either filter or top parameter is empty.

## 6. Concurrency (`patternCheckConcurrencySettings`)
**Logic:**  
Checks concurrency control settings for Apply to each (Foreach) actions.

- **Pass Example:** Apply to each action with concurrency control disabled.
- **Fail Example:** Apply to each action with concurrency control enabled.

## 7. Trigger Condition (`patternCheckTriggerConditionLogic`)
**Logic:**  
Checks if trigger conditions are added to flow triggers.

- **Pass Example:** Flow with trigger condition configured.
- **Fail Example:** Flow with no trigger condition.

## 8. Nested Loops (`patternCheckNestedLoops`)
**Logic:**  
Detects nested loops inside the flow.

- **Pass Example:** Flow without nested loops.
- **Fail Example:** Flow with nested loops.

## 9. Action Count (`patternOptimizeActionCounts`)
**Logic:**  
Checks if flow exceeds 50 actions.

- **Pass Example:** Flow with less than 50 actions.
- **Fail Example:** Flow with more than 50 actions.

## 10. Naming Conventions (`patternCheckConsistentNaming`)
**Logic:**  
Ensures trigger names start with `Trg_` and action names start with `Act_`.

- **Pass Example:** All triggers and actions correctly prefixed.
- **Fail Example:** Action named `Each_Approver` instead of starting with `Act_`.

## 11. Action Note (`patternCheckForActionNote`)
**Logic:**  
Ensures all actions have a note (description).

- **Pass Example:** All actions have notes.
- **Fail Example:** At least one action lacks a note.

## 12. PowerApp Response (`patternCheckPowerAppResponse`)
**Logic:**  
Checks if the flow contains a "Respond to a Power App or flow" action.

- **Pass Example:** No Respond to a Power App or flow action present.
- **Fail Example:** Respond to a Power App or flow action is present.

## 13. Create/Update Inside Loop (`patternCheckCreateUpdateInsideLoop`)
**Logic:**  
Detects Create/Update/Delete actions inside loops for Dataverse and SharePoint.

- **Dataverse Actions:**
  - Add a new row (CreateRecord)
  - Add a new row to selected environment (CreateRecordWithOrganization)
  - Update a row (UpdateOnlyRecord)
  - Update a row in selected environment (UpdateOnlyRecordWithOrganization)
  - Upsert a row (UpdateRecord)
  - Upsert a row in selected environment (UpdateRecordWithOrganization)
  - Delete a row (DeleteRecord)
  - Delete a row from selected environment (DeleteRecordWithOrganization)

- **SharePoint Actions:**
  - Create File (CreateFile)
  - Create Item (PostItem)
  - Delete File (DeleteFile)
  - Delete Item (DeleteItem)
  - Update File (UpdateFile)
  - Update Item (PatchItem)

- **Pass Example:** No Dataverse or SharePoint actions inside loops.
- **Fail Example:** At least one of the above actions is used inside a loop.
