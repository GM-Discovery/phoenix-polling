# Trust Point Allocation Workflow: Initial Bubble.io Implementation

## 1. Conceptual Workflow Overview

### Core Principles
- Annual 1.0 trust point allocation per adult
- 20% annual point decay
- Transparent allocation process
- Simple user interface for point management

## 2. Proposed Bubble.io Workflow Steps

### User Registration and Initial Setup
1. User Creates Account
   - Basic personal information
   - Age verification (must be 10+ to receive points)
   - Pseudonymous identifier generation

2. Annual Point Allocation (January 1st)
   - Automatic system allocation of 1.0 trust points
   - Notification to user about point receipt
   - Display of current point balance

### Point Allocation Mechanism
1. Point Distribution Interface
   - List of available authenticators/organizations
   - Slider or input method to allocate points
   - Real-time balance tracking
   - Validation checks:
     * Cannot exceed 1.0 points total
     * Max 0.1 points to religious/political organizations
     * Minimum allocation increments (e.g., 0.1 points)

### Point Decay Tracking
1. Automated Decay Calculation
   - Backend calculation of 20% point reduction annually
   - Automatic adjustment of point balances
   - Clear visualization of point decay

## 3. Data Model Considerations

### User Object
- Unique Identifier
- Age
- Total Trust Points
- Point Allocation History
- Last Allocation Date
- Decay Tracking

### Authenticator/Organization Object
- Name
- Type (e.g., educational, community, etc.)
- Total Received Points
- Validation Score

## 4. Initial Technical Challenges in Bubble.io

### Data Tracking Challenges
- Implementing precise point decay
- Maintaining accurate allocation history
- Preventing point manipulation

### Recommended Approach
1. Use Bubble's database to track:
   - User points
   - Allocation timestamps
   - Decay calculations
2. Create scheduled workflows for:
   - Annual point reset
   - Decay calculation
3. Implement validation rules to prevent over-allocation

## 5. Minimum Viable Product (MVP) Features

### User Interface
- Point balance display
- Allocation interface
- Simple organization list
- Basic allocation history

### Backend Functionality
- Annual point allocation
- Point decay tracking
- Basic validation checks

## 6. Proof of Concept Workflow

1. User Registration
   - Create user account
   - Verify age eligibility
   - Receive initial trust points

2. Point Allocation
   - Select authenticators
   - Allocate points using simple interface
   - Real-time balance update

3. Decay Simulation
   - Demonstrate annual point reduction
   - Show historical point changes

## 7. Next Development Steps

1. Prototype bare-bones implementation in Bubble.io
2. Manual testing of core allocation mechanics
3. Document technical limitations and workarounds
4. Gather user feedback on initial interface
5. Refine allocation interface and backend logic

## Considerations for Limited Technical Experience

- Start with the simplest possible implementation
- Focus on core principles over technical complexity
- Use Bubble.io's visual programming to reduce coding barriers
- Prioritize user understanding and interface clarity

## Potential Technical Limitations in Bubble.io

1. Precise decimal point tracking
2. Complex decay calculations
3. High-volume data management
4. Advanced security mechanisms

### Mitigation Strategies
- Use built-in numeric fields with rounding
- Implement manual decay calculations
- Start with small user base
- Focus on conceptual demonstration