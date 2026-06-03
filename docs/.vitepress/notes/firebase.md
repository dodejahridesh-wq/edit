---
name: firebase
description: Manage Firebase projects, configure databases (Firestore, Realtime Database), deploy hosting/functions, and orchestrate Cloud Operations.
---
# Firebase Developer & Operations Specialist

This skill provides operational and setup instructions for configuring, developing, and deploying backend applications and static sites using the Firebase suite and Firebase CLI.

## Installation & Login

Ensure the Firebase CLI is installed and authenticated:
-   **Install Firebase CLI**: Install using npm globally: `npm install -g firebase-tools`
-   **Authentication**: Run `firebase login` to authenticate with your Google account.
-   **Verification**: Run `firebase projects:list` to list all accessible Firebase projects.

## Project Initialization

To set up a new project configuration inside a directory:
```bash
firebase init
```
This interactive prompt allows you to configure:
-   **Firestore**: Security rules (`firestore.rules`) and indexes (`firestore.indexes.json`).
-   **Functions**: Typescript/Javascript cloud functions environment under `/functions`.
-   **Hosting**: Directories for serving static web assets (`/dist` or `/public`).

## Deploying Services

Deploy changes to Firebase cloud infrastructure:
-   **Deploy All**: `firebase deploy`
-   **Deploy Specific Feature**: 
    -   Only Hosting: `firebase deploy --only hosting`
    -   Only Functions: `firebase deploy --only functions`
    -   Only Firestore Rules: `firebase deploy --only firestore:rules`

## Local Emulators

Run the Firebase local emulator suite to test rules and cloud functions offline:
```bash
firebase emulators:start
```
This mounts the emulator dashboard locally (typically at `localhost:4000`), allowing sandbox testing of Authentication, Firestore, and Functions.
