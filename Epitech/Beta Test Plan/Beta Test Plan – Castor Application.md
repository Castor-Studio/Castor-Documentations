---

title:          Beta Test Plan Castor Studio
subtitle:       Castor Studio - Desktop Application for video recording and streaming
author:         Castor Team
module:         G-EIP-700
version:        6.0
-------------------

## 1. Project context

Castor is a desktop application for video recording and live streaming. It allows users to create scenes, attach video and audio sources to them, select a scene, and stream or record it in real time.

The application focuses on low-latency scene switching and AI-assisted decision making for live production.

The beta version must validates the following pipeline:
capture → select scene → encode → stream/record.

---

## 2. User Roles

| Role         | Description                                                             |
| ------------ | ----------------------------------------------------------------------- |
| Regular User | Can manage scenes, sources, stream and record and access to AI features |

---

## 3. Feature table

| Feature ID | User role                      | Feature name                            | Short description |
| ---------- | ------------------------------ | --------------------------------------- | ----------------- |
| F1         | Connect Twitch account         | Authenticate with Twitch using OAuth    |                   |
| F2         | Disconnect Twitch account      | Remove Twitch authentication session    |                   |
| F3         | Create a scene                 | Create a new scene container            |                   |
| F4         | Delete a scene                 | Remove an existing scene                |                   |
| F5         | Select a scene                 | Set a scene as active                   |                   |
| F6         | Add a video source to a scene  | Attach a video input to a scene         |                   |
| F7         | Add an audio source to a scene | Attach an audio input to a scene        |                   |
| F8         | Start a recording              | Start recording the active scene        |                   |
| F9         | Stop a recording               | Stop recording and save the file        |                   |
| F10        | Start a stream                 | Start streaming the active scene        |                   |
| F11        | Stop a stream                  | Stop the active stream                  |                   |
| F12        | Switch scene during recording  | Change the active scene while recording |                   |
| F13        | Switch scene during streaming  | Change the active scene while streaming |                   |
| F14        | Configure streaming platform   | Set up RTMP or OAuth streaming          |                   |
| F15        | Enable AI agent mode           | Activate AI suggestions                 |                   |
| F16        | Enable AI autonomous mode      | Allow AI to control scene switching     |                   |
| F17        | Disable AI                     | Disable any active AI mode              |                   |

---

## 4. Success criteria

| Feature ID | Key success criteria                                       | Indicator / Metric               | Result          |
| ---------- | ---------------------------------------------------------- | -------------------------------- | --------------- |
| F1         | Twitch OAuth connection succeeds                           | 10 attempts, ≥90% success        | To be evaluated |
| F2         | Twitch account disconnects correctly                       | 10 attempts, 0 residual session  | To be evaluated |
| F3         | A scene can be created                                     | 15 creations, all visible        | To be evaluated |
| F4         | A scene can be deleted                                     | 10 deletions, no residual data   | To be evaluated |
| F5         | A scene can be selected                                    | 20 selections, 0 failure         | To be evaluated |
| F6         | A video source is added to a scene                         | 15 additions, 0 failure          | To be evaluated |
| F7         | An audio source is added to a scene                        | 15 additions, 0 failure          | To be evaluated |
| F8         | Recording starts without error                             | 10 attempts, ≥90% success        | To be evaluated |
| F9         | Recording stops and file is valid                          | 10 recordings, 100% readable     | To be evaluated |
| F10        | Stream starts successfully                                 | 10 attempts, ≥80% success        | To be evaluated |
| F11        | Stream stops without crash                                 | 10 stops, 0 crash                | To be evaluated |
| F12        | Scene switching during recording does not interrupt output | 20 switches, 0 interruption      | To be evaluated |
| F13        | Scene switching during streaming does not interrupt output | 20 switches, 0 interruption      | To be evaluated |
| F14        | Streaming configuration is usable                          | 5 configs, 100% functional       | To be evaluated |
| F15        | AI agent mode can be enabled                               | 10 activations, 0 failure        | To be evaluated |
| F16        | AI autonomous mode controls switching                      | 20 switches, ≥70% relevant       | To be evaluated |
| F17        | AI can be disabled without side effects                    | 10 disables, 0 residual behavior | To be evaluated |

---

## 5. Conclusion

This beta test plan validates the core workflow of Castor, from scene creation to live streaming and AI-assisted control.

The objective is to ensure:

* scene management is reliable,
* streaming and recording are stable,
* scene switching is seamless,
* AI features integrate correctly into the workflow.

The results will determine the readiness of the application for the next development phase.
