---
description: "Task list for Physical AI & Humanoid Robotics: Complete AI-Native Interactive Textbook"
---

# Tasks: Physical AI & Humanoid Robotics: Complete AI-Native Interactive Textbook

**Input**: Design documents from `/specs/001-physical-ai-robotics/`
**Prerequisites**: plan.md (required), spec.md (required for user stories), research.md, data-model.md, contracts/

**Tests**: The examples below include test tasks. Tests are OPTIONAL - only include them if explicitly requested in the feature specification.

**Organization**: Tasks are grouped by user story to enable independent implementation and testing of each story.

## Format: `[ID] [P?] [Story] Description`

- **[P]**: Can run in parallel (different files, no dependencies)
- **[Story]**: Which user story this task belongs to (e.g., US1, US2, US3)
- Include exact file paths in descriptions

## Path Conventions

- **Single project**: `src/`, `tests/` at repository root
- **Web app**: `backend/src/`, `frontend/src/`
- Paths shown below assume single project - adjust based on plan.md structure

## Phase 1: Setup (Shared Infrastructure)

**Purpose**: Project initialization and basic structure

- [X] T001 Create public GitHub repo with MIT license, README, .gitignore
- [X] T002 Generate full Docusaurus 3 site with classic preset, TypeScript, dark mode, blog disabled, docs-only mode
- [X] T003 AI-generate GitHub Actions workflow for GitHub Pages deploy on main push

---

## Phase 2: Foundational (Blocking Prerequisites)

**Purpose**: Core infrastructure that MUST be complete before ANY user story can be implemented

⚠️ **CRITICAL**: No user story work can begin until this phase is complete

- [X] T004 Generate versioned sidebar.js with Intro → Module 1 → Module 2 → Module 3 → Module 4 → Capstone → Hardware → Appendix
- [X] T005 [P] Integrate Algolia DocSearch (free tier) + fallback to built-in search
- [ ] T006 [P] Add Starboard notebook support for runnable Python/ROS code in-browser
- [ ] T007 [P] Deploy embedded RAG chatbot (FastRAG + Qdrant + Llama-3-8B-Instruct) trained on initial book content
- [ ] T008 [P] Add @docusaurus/plugin-pdf-generation

**Checkpoint**: Foundation ready - user story implementation can now begin in parallel

---

## Phase 3: User Story 1 - Textbook Setup & Basic Navigation (Priority: P1) 🎯 MVP

**Goal**: A learner can clone the repository, set up the Docusaurus site, and navigate its basic features.

**Independent Test**: A user can clone the repository, execute a single command, and access the Docusaurus site locally or via GitHub Pages, then successfully navigate to the introduction chapter.

### Implementation for User Story 1

- [X] T009 [US1] Create `docs/intro.mdx` with an introduction to the textbook.
- [X] T010 [US1] Configure Docusaurus `docusaurus.config.js` for basic site metadata and navigation.
- [X] T011 [US1] Verify Docusaurus site can be built and served locally.
- [ ] T012 [US1] Push initial Docusaurus site to GitHub to trigger GitHub Pages deploy.
- [ ] T013 [US1] Verify deployed GitHub Pages site is accessible.

**Checkpoint**: At this point, User Story 1 should be fully functional and testable independently

---

## Phase 4: User Story 2 - Module 1: Mastering ROS 2 Fundamentals (Priority: P2)

**Goal**: A learner completes Module 1, gaining a foundational understanding of ROS 2 concepts and applying them to a humanoid robot's nervous system.

**Independent Test**: A user can follow Module 1, complete the exercises for ROS 2 nodes, topics, services, actions, parameters, launch systems, Python rclpy, and URDF/Xacro, and successfully visualize a 20+ DoF humanoid in RViz2.

### Implementation for User Story 2

- [X] T014 [US2] Create `docs/modules/module1/_category_.json` for Module 1 sidebar.
- [ ] T015 [US2] Create `docs/modules/module1/1.1-introduction-physical-ai-robotics.mdx` for Introduction to Physical AI & Humanoid Robotics Landscape.
- [ ] T016 [US2] Create `docs/modules/module1/1.2-ros2-from-zero.mdx` covering ROS 2 installation, colcon, rclpy basics.
- [ ] T017 [US2] Create `docs/modules/module1/1.3-urdf-xacro-mastery.mdx` for building a 22-DoF Humanoid Model.
- [ ] T018 [US2] Create `docs/modules/module1/1.4-ros2-components.mdx` covering Nodes, Topics, Services, Actions & Launch Systems.
- [ ] T019 [US2] Add basic ROS 2 Python node example to `docs/modules/module1/1.2-ros2-from-zero.mdx`.
- [ ] T020 [US2] Add URDF/Xacro example for a 20+ DoF humanoid to `docs/modules/module1/1.3-urdf-xacro-mastery.mdx`.
- [ ] T021 [US2] Verify humanoid visualization in RViz2 based on the URDF/Xacro.

**Checkpoint**: At this point, User Stories 1 AND 2 should both work independently

---

## Phase 5: User Story 3 - Module 2: Building the Digital Twin (Priority: P2)

**Goal**: A learner progresses through Module 2, focusing on creating a physics-based digital twin of the humanoid robot in simulation.

**Independent Test**: A user can follow Module 2, build a world in Gazebo/Ignition, add sensors, and successfully spawn and control a simulated humanoid robot.

### Implementation for User Story 3

- [X] T022 [US3] Create `docs/modules/module2/_category_.json` for Module 2 sidebar.
- [ ] T023 [US3] Create `docs/modules/module2/2.1-gazebo-setup-sensor-plugins.mdx` covering Gazebo Harmonic Setup + Sensor Plugins.
- [ ] T024 [US3] Create `docs/modules/module2/2.2-simulating-humanoid.mdx` covering Simulating a Full Humanoid (Gazebo + RViz2 + Foxglove).
- [ ] T025 [US3] Create `docs/modules/module2/2.3-unity-rendering-ros-connector.mdx` covering Unity High-Fidelity Rendering + ROS TCP Connector.
- [ ] T026 [US3] Add Gazebo/Ignition world and sensor plugin examples to `docs/modules/module2/2.1-gazebo-setup-sensor-plugins.mdx`.
- [ ] T027 [US3] Add simulated humanoid control examples via ROS 2 topics/actions to `docs/modules/module2/2.2-simulating-humanoid.mdx`.

**Checkpoint**: All user stories should now be independently functional

---

## Phase 6: User Story 4 - Module 3: Implementing the AI-Robot Brain (Priority: P2)

**Goal**: A learner integrates NVIDIA Isaac Platform tools to create the AI brain for perception and locomotion.

**Independent Test**: A user can follow Module 3, set up NVIDIA Isaac Sim, integrate Isaac ROS GEMs for perception, and achieve bipedal locomotion using Nav2 for their simulated humanoid.

### Implementation for User Story 4

- [X] T028 [US4] Create `docs/modules/module3/_category_.json` for Module 3 sidebar.
- [ ] T029 [US4] Create `docs/modules/module3/3.1-isaac-sim-installation.mdx` covering Isaac Sim & Omniverse Installation (Ubuntu 22.04 + RTX).
- [ ] T030 [US4] Create `docs/modules/module3/3.2-isaac-ros-gems.mdx` covering Isaac ROS GEMs – VSLAM, Stereo, AprilTag, ESS.
- [ ] T031 [US4] Create `docs/modules/module3/3.3-nav2-moveit2.mdx` covering Nav2 for Bipedal Locomotion + MoveIt 2 for Manipulation.
- [ ] T032 [US4] Create `docs/modules/module3/3.4-synthetic-data-replicator.mdx` covering Synthetic Data & Domain Randomization with Replicator.
- [ ] T033 [US4] Add examples of processing sensory data with Isaac ROS GEMs to `docs/modules/module3/3.2-isaac-ros-gems.mdx`.
- [ ] T034 [US4] Add bipedal locomotion using Nav2 in Isaac Sim example to `docs/modules/module3/3.3-nav2-moveit2.mdx`.

**Checkpoint**: All user stories should now be independently functional

---

## Phase 7: User Story 5 - Module 4: Conversational Robotics & VLA (Priority: P1)

**Goal**: A learner builds an end-to-end voice-controlled humanoid robot capable of understanding and executing complex commands.

**Independent Test**: A user can follow Module 4, integrate Whisper, a large language model (LLM), and task & motion planning to enable their simulated (or real) humanoid to understand and execute the voice command "Find the red cup, pick it up, and bring it to me."

### Implementation for User Story 5

- [X] T035 [US5] Create `docs/modules/module4/_category_.json` for Module 4 sidebar.
- [ ] T036 [US5] Create `docs/modules/module4/4.1-whisper-llm-ros-planner.mdx` covering Whisper + GPT-4o/Llama-3 → ROS 2 Task Planner.
- [ ] T037 [US5] Create `docs/modules/module4/4.2-open-vocabulary-detection-grasping.mdx` covering Open-Vocabulary Detection & Grounded Grasping (Grounding DINO + SAM 2).
- [ ] T038 [US5] Create `docs/modules/module4/4.3-end-to-end-voice-controlled-humanoid.mdx` covering End-to-End Voice-Controlled Humanoid (Full Pipeline).
- [ ] T039 [US5] Create `docs/modules/module4/4.4-jetson-orin-deployment.mdx` covering Jetson Orin Deployment – TensorRT Optimization & Latency Tuning.
- [ ] T040 [US5] Add voice-to-action pipeline integration example to `docs/modules/module4/4.1-whisper-llm-ros-planner.mdx`.
- [ ] T041 [US5] Add open-vocabulary detection and grasping examples to `docs/modules/module4/4.2-open-vocabulary-detection-grasping.mdx`.
- [ ] T042 [US5] Create a single ROS 2 launch file for the full voice-controlled humanoid demo.

**Checkpoint**: All user stories should now be independently functional

---

## Phase 8: User Story 6 - RAG Chatbot Integration (Priority: P2)

**Goal**: A learner utilizes the embedded RAG chatbot for quick, accurate, chapter-referenced answers to technical questions.

**Independent Test**: A user can ask a technical question to the embedded RAG chatbot and receive an accurate, chapter-referenced answer within 3 seconds.

### Implementation for User Story 6

- [ ] T043 [US6] Implement FastRAG + Qdrant + Llama-3-8B-Instruct for the RAG chatbot.
- [ ] T044 [US6] Integrate RAG chatbot UI into Docusaurus (e.g., `src/components/RAGChatbot.js`).
- [ ] T045 [US6] Train RAG chatbot on initial textbook content.
- [ ] T046 [US6] Verify RAG chatbot provides accurate, chapter-referenced answers within 3 seconds.

**Checkpoint**: All user stories should now be independently functional

---

## Phase 9: User Story 7 - Jetson Orin Deployment (Priority: P3)

**Goal**: A user successfully deploys the full inference stack to a Jetson Orin Nano/AGX and observes low-latency operation.

**Independent Test**: A user can successfully deploy the full inference stack (Whisper, LLM, perception models) to a Jetson Orin Nano/AGX and observe end-to-end latency of ≤150 ms for voice command execution.

### Implementation for User Story 7

- [ ] T047 [US7] Create `docs/hardware-guide.mdx` for Hardware Guide – RTX Workstation + Jetson Kit + Unitree G1/Go2.
- [ ] T048 [US7] Add instructions for deploying inference stack to Jetson Orin to `docs/modules/module4/4.4-jetson-orin-deployment.mdx`.
- [ ] T049 [US7] Optimize inference stack with TensorRT for ≤150 ms end-to-end latency on Jetson Orin.
- [ ] T050 [US7] Verify end-to-end latency on Jetson Orin.

**Checkpoint**: All user stories should now be independently functional

---

## Phase 10: Capstone & Supporting Chapters

**Purpose**: Final content for the capstone project and appendices.

- [X] T051 Create `docs/capstone.mdx` for Chapter 15: Capstone – “Bring Me the Red Cup” Full Project.
- [X] T052 Create `docs/appendix/troubleshooting.mdx` for Appendix A: Troubleshooting & Common Errors.
- [X] T053 Create `docs/appendix/code-repo.mdx` for Appendix B: Full URDF + Launch Files Repository.

---

## Phase 11: Quality & Deployment Gate

**Purpose**: Final checks and deployment.

- [ ] T054 Run full readability, plagiarism, broken-link, and code-execution checks across all chapters (`/sp.review all-chapters`).
- [ ] T055 Retrain RAG chatbot on final MDX content (`/sp.implement final-rag-train`).
- [ ] T056 Audit project for 100% compliance (`/sp.audit complete`).
- [ ] T057 Final commit and push to trigger GitHub Pages deploy.
- [ ] T058 Verify live URL meets all success criteria (voice-command demo works in simulation).

---

## Dependencies & Execution Order

### Phase Dependencies

- **Setup (Phase 1)**: No dependencies - can start immediately
- **Foundational (Phase 2)**: Depends on Setup completion - BLOCKS all user stories
- **User Stories (Phase 3-9)**: All depend on Foundational phase completion
  - User stories can then proceed in parallel (if staffed)
  - Or sequentially in priority order (P1 → P2 → P3)
- **Capstone & Supporting (Phase 10)**: Depends on all core modules (User Stories 2-5) being complete.
- **Quality & Deployment (Phase 11)**: Depends on all content creation and core features being complete.

### User Story Dependencies

- **User Story 1 (P1)**: Can start after Foundational (Phase 2) - No dependencies on other stories
- **User Story 2 (P2)**: Can start after Foundational (Phase 2) - No dependencies on other stories
- **User Story 3 (P2)**: Can start after Foundational (Phase 2) - Depends on User Story 2 for basic ROS 2 environment.
- **User Story 4 (P2)**: Can start after Foundational (Phase 2) - Depends on User Story 3 for simulated humanoid and environment.
- **User Story 5 (P1)**: Can start after Foundational (Phase 2) - Depends on User Story 4 for AI-powered humanoid with perception and locomotion.
- **User Story 6 (P2)**: Can start after Foundational (Phase 2) - No dependencies on other stories, but requires textbook content for training.
- **User Story 7 (P3)**: Can start after Foundational (Phase 2) - Depends on User Stories 3 & 4 for functional AI-robot brain and VLA pipeline.

### Within Each User Story

- Content creation tasks before verification tasks.
- Core implementation before integration.
- Story complete before moving to next priority (if sequential).

### Parallel Opportunities

- All Setup tasks (T001-T003) can run in parallel.
- Foundational tasks (T004-T008) marked [P] can run in parallel.
- Once Foundational phase completes, User Stories can be worked on in parallel by different team members (respecting story dependencies).
- Within each User Story, content creation tasks can often be parallelized (e.g., T015-T018).

---

## Implementation Strategy

### MVP First (User Story 1 Only)

1. Complete Phase 1: Setup
2. Complete Phase 2: Foundational (CRITICAL - blocks all user stories)
3. Complete Phase 3: User Story 1
4. **STOP and VALIDATE**: Test User Story 1 independently
5. Deploy/demo if ready

### Incremental Delivery

1. Complete Setup + Foundational → Foundation ready
2. Add User Story 1 → Test independently → Deploy/Demo (MVP!)
3. Add User Story 2 → Test independently → Deploy/Demo
4. Add User Story 3 → Test independently → Deploy/Demo
5. Each story adds value without breaking previous stories

### Parallel Team Strategy

With multiple developers:

1. Team completes Setup + Foundational together
2. Once Foundational is done:
   - Developer A: User Story 1 & 5 (P1 stories)
   - Developer B: User Story 2 & 3 (P2 stories, with dependency)
   - Developer C: User Story 4 & 6 (P2 stories)
   - Developer D: User Story 7 (P3 story)
3. Stories complete and integrate independently

---

## Notes

- [P] tasks = different files, no dependencies
- [Story] label maps task to specific user story for traceability
- Each user story should be independently completable and testable
- Verify tests fail before implementing
- Commit after each task or logical group
- Stop at any checkpoint to validate story independently
- Avoid: vague tasks, same file conflicts, cross-story dependencies that break independence
