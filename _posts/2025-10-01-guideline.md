---
layout: post
title: "Growth Boosting and Tracking (GBT) System"
date: 2025-10-01
---

## Complete Workflow Guide v3.0

## 1. System Overview

The Growth Boosting and Tracking (GBT) system accelerates personal capability development through an AI-driven adaptive learning framework. It employs six specialized AI agents that work together through file-based communication to create, execute, and optimize personalized learning strategies.

### Core Value Proposition

- **Accelerate** capability development to achieve goals in minimum time
- **Track** progress with data-driven insights and metrics
- **Adapt** learning strategies based on actual performance
- **Prevent** burnout through intelligent workload management

## 2. System Architecture

### 2.1 Directory Structure

```
/10_Capabilities/       # Capability definitions and requirements
/20_Projects/           # Project goals and milestones  
/30_Input/              # User inputs
  ├── Journal/          # Daily reflections and task records
  └── Schedule/         # Google Calendar & Todoist data
/70_Metrics/            # Success criteria and KPIs
/80_Models/             # Growth Models (learning strategies)
  └── Archive/          # Previous model versions
/90_AI/                 # AI agent workspace
  ├── Action/           # Weekly action cards
  ├── Outcomes/         # Growth Evaluation Reports (GER)
  ├── Schedule/         # Schedule proposals
  ├── Submissions/      # Test results
  ├── Tests/            # Assessment materials
  └── GrowthModelEval/  # Growth Model Reports (GMR)
```

### 2.2 AI Agent Ecosystem

|Agent|Purpose|Creates|Authority|
|---|---|---|---|
|**Growth Model Create AI**|Design learning strategies|Growth Models|Sole authority over `/80_Models/`|
|**Assignment AI**|Generate weekly tasks|Action Cards|Task generation|
|**Test Contents AI**|Create assessments|Tests & Answer Keys|Assessment design|
|**Schedule AI**|Propose time slots|Schedule Proposals|Suggest only, never modify|
|**Growth Analysis AI**|Analyze performance|GER Reports|Performance evaluation|
|**Growth Model Eval AI**|Evaluate model effectiveness|GMR Reports|Model assessment|

## 3. Workflow Process

### 3.1 System Flow
![[Attachment/Pasted image 20251001103218.png]]



### 3.2 Detailed Process Steps

#### Phase 1: Initialization

1. **Project Definition** (`/20_Projects/`)
    - Define goals and objectives
    - Set timeline and milestones
2. **Capability Mapping** (`/10_Capabilities/`)
    - Identify required skills
    - Define proficiency levels
3. **Metrics Establishment** (`/70_Metrics/`)
    - Set measurable success criteria
    - Define evaluation methods

#### Phase 2: Model Creation

**Growth Model Create AI** generates initial model:

- Input: Project goals, capabilities, user constraints
- Output: Complete Growth Model in `/80_Models/`
- Contains: Learning phases, methods, Bloom's Taxonomy progression

#### Phase 3: Weekly Execution Cycle

**Monday - Planning**

1. **Assignment AI** reads:
    - Latest GER from `/90_AI/Outcomes/`
    - Current Growth Model from `/80_Models/`
    - User schedule from `/30_Input/Schedule/`
2. Generates Action Cards in `/90_AI/Action/`

**Tuesday-Thursday - Execution**

1. User works on assigned tasks
2. Records progress in `/30_Input/Journal/`
3. **Test Contents AI** creates assessments when triggered

**Friday - Review**

1. User submits test results to `/90_AI/Submissions/`
2. **Schedule AI** proposes next week's schedule
3. User approves/modifies proposals

**Weekly/As Needed**

1. **Growth Analysis AI** generates GER when:
    - 7 days have passed
    - 3+ new submissions available
2. GER saved to `/90_AI/Outcomes/`

#### Phase 4: Monthly Evaluation

1. **Growth Model Eval AI** analyzes multiple GERs
2. Generates GMR with recommendation:
    - **MAINTAIN**: Continue current model
    - **IMPROVE**: Minor adjustments needed
    - **REPLACE**: New model required
3. If not MAINTAIN, triggers **Growth Model Create AI**

## 4. Key Components

### 4.1 Growth Model

The strategic foundation containing:

- **Core Principle**: Learning philosophy
- **Architecture**: Phased progression plan
- **Mechanisms**: Specific learning methods
- **Metrics**: Success measurements
- **Bloom's Taxonomy**: L1-L6 progression framework

### 4.2 Action Cards

Weekly assignments containing:

- Task description with clear steps
- Success criteria
- Required resources
- Time estimates
- Links to relevant capabilities/projects

### 4.3 Growth Evaluation Report (GER)

Performance analysis including:

- Capability assessment scores
- Learning pattern insights
- Growth velocity calculations
- Risk assessments (burnout, plateau, decay)
- Actionable recommendations

### 4.4 Growth Model Report (GMR)

Model effectiveness evaluation:

- Prediction accuracy vs actual performance
- Success/failure pattern analysis
- ROI assessment
- Improvement recommendations or replacement proposal

## 5. Operational Guidelines

### 5.1 Execution Rules

**Document Management**

- Never create duplicate files on same date - update existing
- All agents read from designated folders
- Only designated agents write to specific folders
- Archive previous versions, never delete

**Agent Communication**

- Agents communicate only through files
- No direct agent-to-agent communication
- Asynchronous processing via file system
- Each agent operates independently

### 5.2 Critical Constraints

|Constraint|Rule|Reason|
|---|---|---|
|**Schedule Modification**|Schedule AI only proposes, never modifies|Respects user autonomy|
|**Model Authority**|Only Growth Model Create AI can modify models|Maintains strategy integrity|
|**Time Utilization**|Maximum 80% of available time|Prevents burnout|
|**Data Minimum**|70% data completeness required for analysis|Ensures accuracy|

### 5.3 Bloom's Taxonomy Progression

|Level|Name|Focus|Assessment|Frequency|
|---|---|---|---|---|
|L1|Recognition|Instant recall|10-second test|Daily|
|L2|Comprehension|Understanding|Explanation task|Weekly|
|L3|Application|Practical use|Scenario problem|Bi-weekly|
|L4|Analysis|Critical thinking|Evaluation task|Monthly|
|L5|Integration|Synthesis|Combination exercise|Quarterly|
|L6|Creation|Innovation|Novel generation|Milestones|

## 6. Implementation Guide

### 6.1 Minimum Viable Setup

Start with essential agents only:

1. Create initial Growth Model (manually or with Growth Model Create AI)
2. Run Assignment AI for weekly tasks
3. Execute and record in Journal
4. Run Growth Analysis AI for feedback
5. Monthly Growth Model Eval AI review

### 6.2 Execution Commands

```bash
# Weekly workflow (Monday)
claude-code run Assignment_AI --generate-weekly
claude-code run Schedule_AI --propose-integration

# After task completion
claude-code run Test_Contents_AI --check-readiness

# Weekly analysis (Friday)
claude-code run Growth_Analysis_AI --generate-ger

# Monthly evaluation
claude-code run Growth_Model_Eval_AI --evaluate-model
```

### 6.3 Error Handling

|Scenario|Response|Fallback|
|---|---|---|
|Insufficient data|Partial analysis with caveats|Wait for more data|
|Agent failure|Continue with available data|Manual intervention|
|Schedule conflict|Generate alternatives|User manual scheduling|
|Model ineffective|Trigger replacement|Maintain current temporarily|

## 7. Success Metrics

### System-Level KPIs

- **Capability Growth Rate**: Target >10% per month
- **Goal Achievement**: >80% milestone completion
- **Time Efficiency**: Actual/Estimated time <1.2
- **Model Effectiveness**: >70% prediction accuracy

### User-Level Indicators

- Consistent engagement (>5 days/week)
- Positive growth velocity trend
- Low burnout risk indicators
- High task completion rate (>85%)

## 8. Continuous Improvement

### Feedback Loops

1. **Short-term** (Weekly): Action → Execution → GER → Next Actions
2. **Medium-term** (Monthly): Performance → GMR → Model Adjustments
3. **Long-term** (Quarterly): Full system review and optimization

### Evolution Mechanism

- System learns from user patterns
- Models evolve based on performance data
- Methods adapt to user's learning style
- Complexity scales with capability growth

## 9. Quick Reference

### File Naming Conventions

```
Action Cards:     YYYY-MM-DD_Action_[CapabilityName].md
Tests:           YYYY-MM-DD_Test_[CapabilityName]_L[Level].md
GER:             YYYY-MM-DD_GER_[ProjectName].md
GMR:             YYYY-MM-DD_GMR_[ModelName].md
Growth Model:    Model_v[X.Y]_[ProjectName]_YYYY-MM-DD.md
```

### Agent Trigger Conditions

- **Assignment AI**: Monday OR new GER available
- **Test Contents AI**: Actions completed OR scheduled test
- **Schedule AI**: New actions/tests created
- **Growth Analysis AI**: Weekly OR 3+ submissions
- **Growth Model Eval AI**: 3+ GERs OR monthly
- **Growth Model Create AI**: GMR recommends change

## 10. Getting Started

1. **Define Your Project** in `/20_Projects/`
2. **List Required Capabilities** in `/10_Capabilities/`
3. **Set Success Metrics** in `/70_Metrics/`
4. **Create Initial Growth Model** in `/80_Models/`
5. **Run Assignment AI** to generate first week's tasks
6. **Execute, Track, Analyze** - let the system adapt to you

---

_The GBT System transforms learning from a linear process into an adaptive, data-driven journey. Each component works together to accelerate your growth while maintaining sustainable progress._
