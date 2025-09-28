# UI Screens and States Documentation

## Overview
This document describes the user interface screens and states for the MVP business consultation tool designed to replace product managers' consultant role with an AI-driven system for business idea validation.

## Application Architecture

### Entry Point
- **Standalone URL**: Direct access point for users
- **No authentication required**: Open access for internal teams
- **Single-page application**: Streamlined user experience

## Screen Descriptions

### 1. Landing Screen
**Purpose**: Initial user engagement and project input collection

**Elements**:
- **Header**: Application title/branding
- **Main prompt**: "What would you like to build today?"
- **Input field**: Large, freeform text area for detailed project description
- **Submit button**: Process the user's input

**User Actions**:
- Enter detailed project description
- Submit for AI analysis

**State**: Initial/empty state

### 2. Analysis Processing Screen
**Purpose**: Show system is working on the user's input

**Elements**:
- **Loading indicator**: Visual feedback that processing is occurring
- **Status message**: "Analyzing your project requirements..."
- **Progress indicator**: Optional progress bar or spinner

**User Actions**:
- Wait for processing to complete
- Cannot interact during this state

**State**: Processing/loading state

### 3. Results Dashboard Screen
**Purpose**: Display comprehensive analysis results

**Elements**:
- **Project summary**: Brief overview of the proposed project
- **Value estimation section**:
  - Annual value calculation (GMV or cost savings)
  - Confidence level indicator
  - Supporting rationale
- **Complexity assessment section**:
  - Team involvement level (single vs multiple teams)
  - Required teams list (backend, frontend, infrastructure, etc.)
  - Complexity scale indicator
- **Information gaps section**:
  - Missing details identified
  - Required team consultations
  - Next steps recommendations
- **Action buttons**:
  - "Request team review" button
  - "Refine project details" button
  - "Start new project" button

**User Actions**:
- Review analysis results
- Request additional team consultations
- Refine project details
- Start a new project

**State**: Results/analysis complete state

### 4. Team Review Request Screen
**Purpose**: Facilitate routing to appropriate product teams

**Elements**:
- **Team selection**: Dropdown/list of available teams
- **Message template**: Pre-filled message for team consultation
- **Additional notes field**: Optional user additions
- **Send request button**: Submit consultation request
- **Back button**: Return to results dashboard

**User Actions**:
- Select target teams
- Customize consultation message
- Send request
- Return to previous screen

**State**: Team routing state

### 5. Project Refinement Screen
**Purpose**: Allow users to provide additional details

**Elements**:
- **Original project description**: Read-only display
- **Additional details form**: Structured input fields
- **Value clarification questions**: AI-generated prompts
- **Complexity refinement options**: Checkboxes/selectors
- **Save changes button**: Update project analysis
- **Cancel button**: Return to results dashboard

**User Actions**:
- Provide additional project details
- Answer clarification questions
- Refine complexity assessment
- Save changes or cancel

**State**: Refinement/edit state

## State Management

### Application States
1. **Initial State**: Landing screen with empty input
2. **Processing State**: Analysis in progress
3. **Results State**: Analysis complete, displaying results
4. **Team Routing State**: Requesting team consultations
5. **Refinement State**: Editing project details
6. **Error State**: Handling processing errors or validation issues

### Data Flow States
- **Input Validation**: Checking user input completeness
- **AI Processing**: Background analysis of project requirements
- **Framework Integration**: Cross-referencing with company documents
- **Result Generation**: Creating comprehensive analysis
- **Team Matching**: Identifying appropriate consultation teams

## User Experience Considerations

### Responsive Design
- Mobile-friendly interface
- Tablet optimization
- Desktop full-feature experience

### Accessibility
- Screen reader compatibility
- Keyboard navigation support
- High contrast mode support
- Clear visual hierarchy

### Performance
- Fast initial load times
- Efficient AI processing feedback
- Smooth transitions between states
- Error handling and recovery

## Integration Points

### External Systems
- Company framework document repository
- Team directory/contact system
- Project management tools
- Communication platforms

### AI Processing
- Natural language understanding
- Value estimation algorithms
- Complexity assessment models
- Team requirement matching
