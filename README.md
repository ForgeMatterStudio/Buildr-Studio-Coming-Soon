<p align="center">
  <img src="assets/banner-en.png" alt="Buildr Studio" width="100%">
</p>

<p align="center">
  <a href="README.md"><strong>English</strong></a>
  •
  <a href="README.pt-BR.md">Português</a>
</p>

---

# Buildr Studio

### Android development. Reimagined for mobile.

Buildr Studio is a mobile-first Android development environment by **ForgeMatter**, designed to make real Android development possible directly from phones and tablets.

It is not intended to be a simplified code editor or a companion app for a desktop IDE.

The goal is a complete development workspace where you can create, edit, analyze, build, test, preview, manage and prepare Android applications for distribution — from one device.

> **Buildr Studio is currently under active private development.**

---

## Build Android apps from anywhere

Buildr brings the essential parts of a modern Android development workflow into an interface designed from the ground up for mobile devices.

Create a project.

Write Kotlin or Java.

Navigate the project structure.

Work with Git and GitHub.

Run builds.

Inspect errors and diagnostics.

Use a real project terminal.

Preview your application.

Prepare releases.

All without requiring a traditional desktop development environment for the core workflow.

---

## What Buildr Studio is being built to do

### Code Editor

A development-focused editor designed for real Android projects.

Planned and evolving capabilities include:

- Kotlin and Java editing
- XML and Android resource editing
- Syntax highlighting
- Line numbers
- Multiple open files
- Project file tree
- Search and replace
- Undo and redo
- Autosave
- Fast navigation between files and symbols
- File and line diagnostics
- Error and warning markers directly in the editor
- Quick fixes when a safe correction is available
- Large-file optimized navigation
- Persistent project and editor state
- Adaptive file panel for compact and large screens

The goal is to progressively bring the editing experience closer to what developers expect from a real IDE.

---

## Real-time diagnostics

Buildr is being designed to detect problems before a build whenever possible.

Diagnostics may include:

- Kotlin errors
- Java errors
- XML syntax problems
- AndroidManifest issues
- Gradle configuration problems
- Missing or invalid project files
- Invalid dependencies or configuration
- Warnings and informational diagnostics

Errors and warnings are intended to appear in multiple places:

- directly on the affected line
- in the editor gutter
- in the status bar
- in the Problems/Diagnostics panel
- inside build details when relevant

When possible, Buildr will also offer a direct path to the affected file and line.

---

## Android and Gradle awareness

Buildr is not being built as a plain text editor.

The project model is designed to understand Android-specific information such as:

- modules
- application ID and namespace
- AndroidManifest configuration
- Gradle structure
- variants and tasks
- SDK configuration
- project dependencies
- launch activities
- build configuration
- project version information

Gradle state and project diagnostics are intended to stay synchronized with the workspace automatically.

---

## Builds

Buildr can initiate and follow Android builds while keeping the development workspace separate from the build infrastructure itself.

The build experience is being designed around:

- build preflight checks
- explicit build confirmation
- build progress
- queued and running states
- build history
- detailed build steps
- duration
- resulting artifacts
- complete logs
- compiler error extraction
- direct navigation from errors to the Editor
- background build tracking
- notifications when important build states change

Buildr should identify the actual compiler error whenever possible instead of only showing generic Gradle failure messages.

---

## Build from the project menu

Projects that already have a valid build configuration will support a fast build flow directly from the Projects area.

Before starting, Buildr can perform a preflight and report blockers such as:

- invalid Gradle state
- missing files
- invalid Manifest
- unavailable GitHub integration
- unresolved local changes
- missing build configuration
- critical diagnostics

If something requires attention, Buildr should show what is wrong and where to fix it instead of failing silently.

---

## Integrated Terminal

Buildr Studio is being designed with a first-class terminal connected to the same real project workspace used by the Editor.

The terminal is planned to support:

- persistent shell sessions
- multiple sessions
- command history
- autocomplete
- file operations
- Git workflows
- clickable `file:line` references
- access to project tools
- interaction with the same files used by the Editor

Changes made in the Terminal should immediately be reflected in:

- the Editor
- the project tree
- diagnostics
- Git state
- project analysis

---

## Buildr CLI

A dedicated `buildr` command-line interface is planned to expose Buildr capabilities directly from the Terminal.

Planned commands include operations such as:

- `buildr project`
- `buildr analyze`
- `buildr problems`
- `buildr sync`
- `buildr build`
- `buildr status`
- `buildr logs`
- `buildr artifact`
- `buildr git`

The CLI and graphical interface are intended to operate on the same project state instead of acting as separate environments.

---

## Git and GitHub

GitHub is a core part of the Buildr workflow.

Buildr is being designed to support:

- importing projects from GitHub
- repository synchronization
- branches
- commits
- project updates
- build integration
- Git status
- remote project awareness
- GitHub Actions-backed workflows where applicable

The GitHub indicator in Buildr reflects the actual synchronization state instead of acting as a decorative connection icon.

---

## Smart project updates

When importing a ZIP that belongs to a project already available in Buildr, the application can identify that relationship instead of blindly creating a duplicate.

The update workflow is designed to:

- identify the existing project
- compare project identity
- show added files
- show modified files
- show removed files
- create a safety snapshot
- update the existing project
- support rollback when an update fails
- allow importing as a separate copy when desired

The goal is safer project evolution without forcing the user to manually replace complete project folders.

---

## Live View

Live View is being developed as a real application preview system.

The goal is not to generate a fake visual approximation of an Android application.

Buildr and its dedicated Preview Host are being designed to:

- identify the project's real launch configuration
- establish an isolated preview runtime
- display the application inside a dedicated preview surface
- react to project changes
- preserve the fidelity of the real application

The Preview Host is designed as a companion component distributed together with compatible versions of Buildr Studio.

Live View remains under active development.

---

## Project management

Buildr provides a unified workspace for local and GitHub-backed projects.

Project workflows are being designed to include:

- new Android project creation
- ZIP import
- GitHub import
- project identification
- project update detection
- project duplication
- contextual project actions
- project-specific build configuration
- persistent workspace state

---

## Build details and artifacts

A completed build should provide more than a green success indicator.

Buildr is being designed to expose:

- compiled version
- previous version
- build variant
- task
- execution duration
- individual build stages
- generated artifact information
- complete logs
- relevant compiler diagnostics
- save and share actions where appropriate

---

## AI-assisted development

Buildr Studio is planned to include an AI assistance layer for development and diagnostics.

When sufficient technical context is available, Buildr may offer actions such as:

- explain a build error
- analyze compiler diagnostics
- identify likely root causes
- suggest code changes
- generate a proposed patch
- explain Gradle problems
- assist with project configuration

AI-generated changes must not be applied silently.

When a code modification is proposed, Buildr is intended to show the change and require explicit user approval before applying it.

---

## Mobile first

The phone experience is being designed to remain capable on its own.

Core development functionality should not require a tablet.

On compact screens, Buildr uses dedicated surfaces for tools such as:

- Editor
- Terminal
- Projects
- Builds
- Home

Panels and contextual tools adapt to the available space.

---

## Built for tablets too

Larger displays are planned to unlock a richer workspace without creating a separate product.

On tablets, Buildr is expected to support layouts such as:

- persistent project tree
- editor and terminal at the same time
- docked terminal
- Problems and output panels
- Live View alongside development tools
- resizable panels
- multi-panel workspace
- keyboard and mouse optimized interactions

The same project, session and terminal state should move between compact and expanded layouts.

---

## Buildr Showcase

A future **Buildr Showcase** is planned as a public catalog for applications created with Buildr Studio.

Developers will be able to present their apps with information such as:

- application name
- description
- screenshots
- release information
- version
- developer information
- official distribution links

The Showcase is not intended to become an APK hosting service.

Applications will point users to official distribution locations provided by their developers.

A future **My Showcase** area is also planned for Buildr accounts.

---

## Buildr Community

A dedicated Buildr Community experience is planned as part of the wider ForgeMatter ecosystem.

The goal is to create a place where Buildr users can:

- discover projects
- exchange development knowledge
- discuss Android development
- share workflows
- help other Buildr users
- discover community resources
- follow Buildr ecosystem updates

The first community experience may be connected to GitHub before evolving into deeper Buildr integration.

---

## Distribution Assistant

Buildr is planned to help developers prepare Android applications for distribution.

The Distribution Assistant is intended to guide users through tasks such as:

- release configuration
- version preparation
- signing configuration
- release validation
- artifact preparation
- distribution readiness checks

Buildr Studio itself is **not planned for distribution through Google Play**.

Official Buildr availability and downloads will be provided through ForgeMatter-controlled channels.

---

## Buildr Preview Host

Some advanced preview capabilities use a dedicated Buildr Preview Host.

Compatible versions of the Preview Host are intended to be distributed together with Buildr Studio rather than requiring users to manually download or build a separate component.

Buildr verifies compatibility before using the Host.

---

## Security by design

Buildr is being developed under the assumption that distributed Android applications can be inspected and reverse engineered.

For that reason, sensitive authorization and security decisions are not intended to rely on hiding logic inside the APK.

The architecture is being designed around principles such as:

- server-side authorization
- short-lived and revocable credentials
- secure token handling
- protected local sensitive data
- minimal exposure of secrets
- integrity checks where appropriate
- separation between client and privileged infrastructure

---

## What's next

Buildr Studio is still evolving.

Some functionality shown or described in this repository may be:

- already implemented
- partially implemented
- under active development
- planned for a future release

The public product experience will continue to change as Buildr approaches its first public versions.

---

## Beta testing

A public beta may be made available before the stable release.

Beta builds may be published as controlled pre-releases and can be replaced or removed as development progresses.

Beta software may contain unfinished functionality, compatibility limitations and known issues.

Official beta availability will always be announced through ForgeMatter-controlled channels.

---

## Release status

**Current status:** Private development

**Public download:** Not available yet

**Public beta:** Planned / under evaluation

**Stable release:** To be announced

---

## About ForgeMatter

ForgeMatter is an independent software studio building ambitious tools for developers and creators.

**Buildr Studio is a ForgeMatter product.**

---

## Repository purpose

This is the public informational repository for Buildr Studio.

It is used for:

- product information
- development status
- public announcements
- beta information
- release information
- official Buildr Studio links

The Buildr Studio source code and internal infrastructure are maintained separately.

---

## Licensing

Buildr Studio is proprietary software.

This repository does not grant permission to copy, modify, redistribute or reuse the Buildr Studio application or its source code.

© 2026 ForgeMatter. All rights reserved.
