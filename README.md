# SignBridge — Beyond Barriers

**A Two-Way Indian Sign Language Translation Platform Powered by AI**

SignBridge is an accessibility-focused software solution designed to reduce communication barriers between Indian Sign Language (ISL) users and people who do not understand sign language. It aims to translate sign language into text and speech, while also converting spoken or typed responses into sign-based visual output.

The project explores movement-aware deep learning using a **Spatial-Temporal Graph Convolutional Network (ST-GCN)** to recognise sign language from body-landmark sequences.

## Project Details

| Field | Details |
|---|---|
| Project Name | SignBridge |
| Team Name | Beyond Barriers |
| Problem Statement | Solutions for Specially-Abled |
| Domain | Artificial Intelligence, Accessibility, Computer Vision |
| Institution | VIT Chennai |
| Event | SCOPE Mission '26 – Experto Innovatum with BIS |

## The Problem

Deaf and hard-of-hearing individuals who communicate using Indian Sign Language may face difficulties in everyday interactions at hospitals, banks, educational institutions, workplaces, and public service counters.

Common barriers include:

- Limited availability of sign language interpreters.
- Communication delays when relying on written or typed messages.
- Lack of accessible two-way communication tools.
- Reduced independence and privacy when another person must interpret conversations.

Speech-to-text tools alone do not provide a complete solution because sign language has its own linguistic structure and cannot be treated simply as spoken language expressed through hand movements.

## Our Solution

SignBridge proposes a two-way communication interface connecting sign language, text, and voice.

### 1. Sign Language to Text and Voice

1. Capture signing through a compatible camera.
2. Extract hand, arm, and other relevant body landmarks.
3. Process landmark sequences using a sign-recognition model.
4. Display the predicted sign as text.
5. Allow the user to review the sentence before optional voice output.

### 2. Speech or Text to Sign

1. Accept spoken input or typed text.
2. Convert the input into supported phrases or words.
3. Display corresponding sign-language clips or a visual signing representation.
4. Use fingerspelling as a fallback for supported letters and unfamiliar words.

The proposed system is intended to work with ordinary compatible camera hardware, without requiring specialised gloves or motion sensors.

## Key Features

- **Live sign recognition:** Recognise supported signs through a camera.
- **Fingerspelling:** Support letter-by-letter communication.
- **Sentence builder:** Combine recognised signs into a sentence for user review.
- **Speech output:** Read confirmed text aloud.
- **Speech-to-sign:** Provide visual sign output for supported spoken or typed phrases.
- **Everyday phrase packs:** Organise useful expressions for common situations.
- **Emergency assistance:** Provide a prominent help message for urgent communication.
- **Learn mode:** Help users explore supported signs.
- **Accessible interface:** Use readable text, high contrast, clear controls, and visual feedback.
- **Browser-based interaction:** Explore camera-based sign detection in a compatible browser.

Feature availability depends on the implementation and the supported vocabulary.

## Proposed Technology

| Component | Purpose |
|---|---|
| Python | Model development and experimentation |
| MediaPipe | Body-landmark extraction |
| Spatial-Temporal Graph Convolutional Network (ST-GCN) | Learning spatial relationships and movement patterns |
| Browser camera APIs | Camera-based input |
| Speech recognition | Spoken input |
| Text-to-speech | Spoken output |
| HTML, CSS and JavaScript | User interface and browser interaction |

*This table describes the proposed technology stack. It should not be interpreted as confirmation that every component has already been implemented.*

## How ST-GCN Fits the Project

Sign language is dynamic: the movement of a hand and its relationship with other body landmarks over time can carry meaning.

The proposed recognition pipeline is:

1. **Capture:** Collect a short sequence of video frames.
2. **Landmark extraction:** Detect relevant body landmarks.
3. **Normalisation:** Prepare landmark coordinates for model input.
4. **Graph construction:** Represent landmarks as nodes and their spatial and temporal relationships as edges.
5. **Recognition:** Process the graph sequence using an ST-GCN model.
6. **Prediction:** Generate a prediction for one of the supported signs.
7. **Communication:** Display the recognised text and provide optional speech output.

The proposed input may contain approximately 30–60 frames of landmark coordinates, depending on the implementation.

## Proposed System Workflow

```text
Camera Input
     |
     v
Landmark Extraction
     |
     v
Coordinate Normalisation
     |
     v
Spatial-Temporal Graph
     |
     v
ST-GCN Sign Recognition
     |
     v
Predicted Sign
     |
     v
Sentence Builder and User Confirmation
     |
     v
Text and Optional Voice Output
```

The reverse communication flow accepts speech or typed text and maps it to available sign clips or fingerspelling output.

## Demonstration Scope

The initial demonstration is intended to focus on a manageable vocabulary rather than claiming complete Indian Sign Language translation.

Planned demonstration components include:

- A controlled vocabulary of approximately 10–15 moving daily-life signs.
- Alphabet or fingerspelling support.
- Landmark or skeleton visualisation.
- Comparison with a still-frame recognition baseline.
- Spoken output for confirmed text.
- Speech-to-sign or typed-text-to-sign output.
- An emergency communication button.
- Accessibility checks for the interface.
- Browser-based sign detection where supported.

Actual vocabulary coverage and recognition performance must be established through testing.

## Accessibility and Responsible Design

Accessibility is a central design objective. The proposed interface considers:

- Text alternatives for spoken information.
- Captions or visible text for speech input.
- Alternative interaction methods, including typing and touch.
- Keyboard accessibility and visible focus indicators.
- High contrast and resizable text.
- Visual feedback for important events.
- User confirmation before speaking recognised sentences.
- Privacy-conscious handling of camera input.

The design is intended to be reviewed against applicable requirements in **BIS IS 17802 (Part 1)**. A standards reference does not, by itself, establish compliance or certification.

## Limitations and Challenges

The project recognises several technical and practical challenges:

- Limited training data for the supported signs.
- Differences in signing style, speed, camera angle, and lighting.
- Signs that require facial expressions or broader body movement.
- Ambiguity between visually similar signs.
- Recognition errors that could change the intended message.
- Limited vocabulary in an initial prototype.
- Privacy considerations when handling camera or speech input.

The system should communicate uncertainty appropriately and allow users to correct predictions instead of treating every prediction as reliable.

## Future Scope

Potential future enhancements include:

- Expanding the supported ISL vocabulary.
- Incorporating facial expressions and more complete body movement.
- Recognising continuous signing and longer sentences.
- Improving robustness across users and recording conditions.
- Developing a mobile application.
- Exploring video-call integration.
- Supporting additional regional languages.
- Conducting usability studies with members of the Deaf community.
- Evaluating recognition accuracy, latency, and accessibility.

## Project Impact

SignBridge aims to make everyday communication more accessible by helping ISL users and non-signers exchange information through familiar text, voice, and visual signing interfaces.

Its long-term value depends not only on model performance but also on usability, linguistic validity, privacy, reliability, and feedback from the people the system is intended to serve.

> Everyone should be able to talk to everyone, with or without a voice.

## Team — Beyond Barriers

| Team Member | Registration Number | Role |
|---|---|---|
| Priyanka S | 23MIA1032 | Team Lead |
| Kavya N | 23MIA1125 | Team Member |
| Sivasankari N | 23MIS1152 | Team Member |
| Jegapreetha K | 23MIS1032 | Team Member |
| Naveen Raj R | 23MIS1129 | Team Member |

---

*SignBridge is an accessibility-focused project prototype. It is not a replacement for qualified interpreters in high-stakes medical, legal, or emergency situations.*
