# Release Focused Development

## Table of Contents

  1. [Key Terms](#1-key-terms)
  2. [Maintenance](#2-maintenance)
    1. Application Owner
    2. Issue tracking
  3. [Planning](#3-planning)
    1. Time management
    2. Project Calculation
    3. Research
    4. Release planing
    5. Determining Development Take-over date
  4. [Single Release](#4-single-release)
    1. Development Take-over
    2. Due Date Manifest
    3. Daily stand-up
    4. QA Date
    5. Release

## 1. Key Terms

  **"Each Developer has only one Release to do in every single moment."**

  - **Release Due Date**
    Most important date in process

  - **System Engineer**

    Developer/Manager responsible for:
      + development patterns
      + system architecture
      + consulting tech solutions
      + **Project Calculation**
      + Define key terms **Ubiquity language**

  - **Application Owner**

    Developer, who is responsible for:
      + fixing the application
      + maintaining repository
      + merging pull-requests
      + deploying application

  - **Release Leader**

    Developer and member of Release Team, who is reponsible for:
      + manifesting **Release Due Date**
      + balancing tasks between Release Team members
      + be in time

  - **Developer and Skill**

    Each developer has some Skills :)

  - **Task**

    Some work assigned **exactly** to one Skill or one Developer

  - **QA**

    Process of assuring quality. **Tester** will write down all issues which must be
    solved by **Release Team** or **Product Owner**. It has specified duration
    from planning (5-25% of Development time)

  - **QA Date**

    The date, when all Release task must be done and Applications deployed
    on testing environments.

  - **Product Owner**

    Manager responsible for:
      + Solution reflects customer needs
      + Delivering required product design to Developers
      + Consulting solutions

## 2. Maintenance

  1. **Application Owner**
  1. **Issue Tracking**

## 3. Planning

  1. **Time management**

    - **Planned / Non-planed time ratio**

      Each Developer has work hours for developing Planned tasks (Planned time)
      and time for other responsibilities (consulting, bugfixing, maintenance).
      For example: `6h/2h (planned/non-planed)`
        + `~6h/2h` for Developers
        + `~5h/3h` for Application Owners
        + `~4h/4h` for System Engineers

  2. **Project Calculation**

    - Is made by **System Engineer**
    - Whole project is split by features into Tasks
    - Each Task is assigned to just one Skill
    - Each Task receives time estimation in hours (1-24)
    - Project receives 0-30% time reserve depending on Complexity
    - Project receives 5-20% time reserve for QA

    ```
                  Baseline
                      |
    serverside skill: | -- serverside tasks -- | R* |                  |    |
    app skill:        |   | --- native appplication tasks --- | - R* - | QA |
    coding skill:     |              | - coding tasks - | R* |         |    |
                      |                                                     |
                      | <---------------- project duration ---------------->|

    R* = Reserve (development time X reserve %)
    QA = (development time X reserve %) X qa %
    ```

  3. **Research = Resolving unestimateable tasks**

    Estimate of tasks without obvious solution clarified by Research.
    Research is special task with limited duration in advance and list of key questions.
    Answers of questions should lead to precise estimate. Output is in the form
    of answered questions and sometimes working prototype.

  4. **Release planing**

    Each Release has:

      + **priority** (releases are sorted)
      + maximum of assigned Developers (1-n)
      + duration of **QA** and duration of Development by skill

    So it'ts possible to calculate Release duration.

  5. **Determining Development Take-over date**

    Release is assigned to first available developers: **The Release Team**
    First possible date is date for Take-over is project start.

    ```
                P2 takeover                 P1 release
                      |                          |
    Dev 1: - Proj.1 - | ---- Proj.2 ---- | P1-QA | --- Proj.2 ---
    Dev 2: ---- Proj.1 ---- | - Proj.2 - | P1-QA | --- Proj.2 ---
    Dev 3: ---------- Proj.1 ----------- | P1-QA || --- Proj.3 --
                                                  |
                                            P3 takeover
    ```

  6. **Descripting tasks**

    Each task should be sufficiently described before development take-over.
    It must contain:

      + Sentence: **Who** needs to do **what** and **why**

## 4. Single Release

  ```
       Take Over    Manifest                                QA Date  Release
           |            |                                       |      |
  Leader   | ---------- | -- task --- | -- task -- | -- task -- |      |
  Dev2     | - ~2-3wh - | - task - | - other task -- | - task - |  QA  |
  Dev3     | ---------- | - possibly other project - | - task - |      |
  ```

  1. **Development Take-over**

    Starts with meeting, when Release is presented to Release team by
    Product Owner and System Engineer. Release is now divided in tasks.

  2. **Due Date Manifest**

    Release Team with Relase Leader will pick their tasks to be
    most eficcient. They will have **2h-1d to think out solution, write
    down Subtasks and estimate its duration.** Maximum duration of subtask
    should be 4 hours.
      + Team estimates should be compared with **System Engineer** estimates.
      + Determine the **QA Date**
      + Then, team will manifest their **Release Due Date**

  3. **Daily stand-up**

    **Release Team** and **Product owner** will each 1-2 days discuss current
    state. **Not solving problems.** In 10 minutes each member just presents:

      + what's done
      + what's blocking
      + everything is in time

    When it's needed, **Release leader** will reasign tasks or arrange
    meetings to solve problems.

  4. **QA Date**

    The day when QA begins. Everything must be developed and deployed to be able to
    make test.

      + Tester will write down all found issues
      + Then tester will discuss all issues with **Release Leader**
        and **Product Owner**
      + **Release Leader** with **Release Team** will pick and solve
        issues
      + Repeat

  5. **Release**

    **Application Leader** and **Product Owner** must confirm the Release Date.