# Example: ESPAORA (SwiftUI)

Request: "Prepare this existing iOS app for safe future collaboration. Do not change Swift files."

Recommended mode: `setup`.

Agent actions: inspect `.xcodeproj`/`.xcworkspace`, Swift entry point, actual views/models/services, asset catalogs, local persistence, Git status and remotes; create factual README/PROJECT_CONTEXT/AGENTS; review `.gitignore`; commit only safe documentation changes; push only to confirmed private remote. Do not claim simulator scenarios work without inspecting code. Do not rewrite SwiftUI screens or create folders simply to match a preferred architecture.

Expected report: exact files changed, branch, commit SHA, private remote verification, push outcome, ignored critical resources, remaining manual steps and unperformed build checks.