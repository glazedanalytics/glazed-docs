# Understanding Glazed

Learn the core concepts and purpose of Glazed's visual analytics approach.

## What is Glazed?

Glazed is a revolutionary analytics tool designed to replace traditional tracking spreadsheets with a Figma-integrated analytics process. Instead of managing complex documentation separately from your designs, Glazed creates a direct connection between your visual interface and your analytics implementation.

## The Problem We Solve

Traditional analytics implementation faces several challenges:

### Disconnected Documentation
- Tracking requirements live in spreadsheets or documents
- Design changes don't automatically update tracking specs
- Developers struggle to understand context from static documentation

### Communication Gaps
- Designers, product managers, and developers work from different sources of truth
- Requirements get lost in translation between teams
- Implementation doesn't match original intent

### Maintenance Overhead
- Spreadsheets become outdated quickly
- No visual reference for what elements need tracking
- Difficult to audit existing implementation

## Glazed's Solution

![Glazed Visual Tracking Approach](images/glazed-intro-overview.png)
*Glazed's visual approach to connecting design and analytics*

### Visual Event Mapping
Glazed links Figma design elements directly to analytics events, creating a visual workflow that streamlines implementation. When you look at a design element, you can immediately see:
- What events should fire when users interact with it
- What properties those events should contain
- The context and purpose of each tracking point

### Single Source of Truth
- Events are defined once and reused across multiple elements
- Changes to event definitions automatically propagate everywhere  
- Design and tracking specifications stay in sync

![Design to Tracking Workflow](images/design-to-tracking-workflow.png)
*How Glazed connects design elements to tracking implementation*

### Developer-Friendly Workflow
- See exactly which elements need tracking implementation
- Understand the business context behind each event
- Get precise specifications without guesswork

## Core Philosophy

**"Analytics should be as visual and intuitive as the interfaces we build."**

Instead of translating between design mockups and tracking spreadsheets, Glazed makes your analytics specification a natural extension of your design process. This reduces errors, improves collaboration, and makes implementation more efficient.

## Key Benefits for Developers

### Clarity and Context
- Understand what to track by seeing it in context
- Reduce back-and-forth with product and design teams
- Implement with confidence knowing requirements are clear

### Consistency
- Standardized event structure across your application
- Reusable event definitions prevent duplication
- Automated validation ensures correct implementation

### Efficiency
- Faster implementation with clear visual guides
- Less time spent deciphering documentation
- Immediate feedback when requirements change

## Getting Started

The next sections will walk you through Glazed's unique approach to event tracking and show you how to effectively work with our tools to implement analytics in your applications.

Ready to dive deeper? Let's explore [Event vs Element Level Tracking](event-vs-element-tracking.md) to understand Glazed's core tracking methodology.