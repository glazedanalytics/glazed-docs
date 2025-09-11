# Link Events to Design Elements

Connect your imported events to specific design elements in your Figma files to create a comprehensive tracking plan.

## Video Tutorial

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%;">
  <iframe src="https://www.youtube.com/embed/rNZR3MsLF2Y" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
</div>

## Prerequisites

Before linking events, ensure you have:

- **Figma file imported** into your Glazed project
- **Tracking schema imported** (optional - you can create events on the fly)

## Linking Process

### 1. Select Design Elements

1. Navigate to your imported Figma file in Glazed
2. Browse through your screens and frames
3. Click on interactive elements (buttons, links, forms, etc.)
4. Glazed will highlight selectable elements

### 2. Assign Events

For each design element, you can:

#### Assign Existing Events
1. Select a design element
2. Choose from your imported event schema
3. Configure any element-specific properties
4. Save the assignment

#### Create New Events
1. Select a design element
2. Click "Create New Event"
3. Define the event name and properties
4. The event will be added to your schema automatically

### 3. Configure Event Properties

When linking events, you can:

- **Set default values** for event properties
- **Map dynamic values** from the design context
- **Add element-specific properties** that differ from the canonical event

## Event Management

### Unlinking Events

To remove an event from a design element:

1. Select the linked element
2. Click "Unlink Event"
3. Confirm the removal

### Deleting Events

To completely remove an event from your project:

1. Navigate to your event schema
2. Find the event to delete
3. Click "Delete Event"
4. Confirm - this will remove all instances

## Best Practices

### Element Selection

- **Focus on user actions**: Buttons, links, form submissions
- **Track key interactions**: Navigation, feature usage, conversions
- **Be comprehensive**: Don't miss important user touchpoints

### Event Organization

- **Group related events**: Use consistent naming conventions
- **Maintain hierarchy**: Parent events with child variations
- **Document context**: Add notes about when events should fire

### Property Management

- **Consistent naming**: Use the same property names across similar events
- **Meaningful values**: Ensure properties provide actionable insights
- **Required vs. optional**: Clearly distinguish essential properties

## Advanced Features

### Bulk Assignment

For similar elements across multiple screens:

1. Select multiple elements using Cmd/Ctrl+click
2. Choose "Bulk Assign Event"
3. Select the event to assign to all elements

### Event Inheritance

Child elements can inherit events from parent containers while adding their own specific tracking.

## Quality Assurance

### Review Your Links

- **Check coverage**: Ensure all important interactions are tracked
- **Validate properties**: Confirm all required properties are set
- **Test scenarios**: Think through user flows and edge cases

### Export for Review

Export your event mapping for team review:

1. Go to Project Settings
2. Click "Export Event Map"
3. Share with stakeholders for validation

## Next Steps

After linking events to your design, proceed to [Create Event Properties and User Properties](create-properties.md) to define the data structure for your tracking implementation.