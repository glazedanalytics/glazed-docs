# Finding and Navigating Events

Learn how to efficiently search, filter, and navigate your event schema in Glazed to quickly find the tracking information you need.

## Overview

As your analytics implementation grows, efficiently finding and understanding your events becomes crucial. Glazed provides powerful search and navigation tools to help developers quickly locate event definitions and understand their implementation requirements.

**Estimated Time**: 5-10 minutes to master these navigation techniques.

## Event Search

### Search by Event Name

The fastest way to find a specific event is by searching for its name:

1. Use the search bar at the top of the Glazed interface
2. Type the event name (e.g., "login", "purchase", "signup")
3. Results appear instantly as you type
4. Click on the event to view its complete definition

### Search by Properties

You can also search for events by their properties:

1. Enter property names in the search bar (e.g., "user_id", "product_category")
2. Glazed will show all events that include those properties
3. Useful for finding related events or ensuring consistency

### Advanced Search Tips

- **Partial matching**: Search works with partial event names
- **Case insensitive**: "LOGIN" will find "login" events
- **Multiple terms**: Search for "user login" to find user-related login events
- **Property search**: Use "property:value" format for specific searches

## Event Filtering

### Filter by Status

Events in Glazed can have different statuses to help you understand their lifecycle:

- **Active**: Currently being tracked in production
- **Draft**: In development, not yet implemented
- **Deprecated**: Being phased out but still firing
- **Archived**: No longer in use

To filter by status:
1. Click the "Filter" button in the event list
2. Select one or more status types
3. The list updates to show only matching events

### Filter by Implementation Status

- **Implemented**: Events with code already deployed
- **Pending**: Events defined but not yet coded
- **Needs Review**: Events that require validation

### Filter by Team or Owner

- Filter events by the team or person responsible
- Useful in large organizations with multiple analytics owners
- Helps focus on events relevant to your current project

## Navigation Patterns

### Event List View

The main event list provides an overview of all events:

- **Event Name**: Click to view detailed definition
- **Description**: Brief summary of what the event tracks
- **Status Badge**: Visual indicator of event status
- **Property Count**: How many properties the event includes
- **Last Modified**: When the event was last updated

### Event Detail View

When you click on an event, you'll see:

- **Complete property list** with types and descriptions
- **Implementation examples** in multiple languages
- **Related events** that share similar properties
- **Element instances** showing where this event is used in designs
- **Change history** for tracking modifications

### Canvas View

The Canvas View shows events in the context of your design:

![Canvas View](images/canvas-view.png)
*Canvas View showing events in the context of your design*

1. Navigate to a specific screen or flow in your Figma file
2. See which elements have events assigned
3. Click on any element to view its event configuration
4. Understand the user journey and event sequence

## Efficient Workflows

### For New Features

1. **Search existing events** first to avoid duplication
2. **Filter by status** to find similar active events
3. **Review related events** for consistency
4. **Check implementation examples** for proper format

### For Debugging

1. **Search by event name** to find the canonical definition
2. **View all element instances** to see different implementations
3. **Check status** to ensure the event is still active
4. **Review change history** for recent modifications

### For Code Reviews

1. **Filter by pending status** to see new events needing implementation
2. **Search by property names** to ensure consistent naming
3. **Check implementation examples** for proper syntax
4. **Validate against event definitions** for completeness

## Quick Reference

### Keyboard Shortcuts

- `Cmd/Ctrl + K`: Open search
- `Cmd/Ctrl + F`: Find in current page
- `Escape`: Close search/filter panels
- `Enter`: Navigate to first search result

### Search Operators

- `name:login` - Find events with "login" in the name
- `property:user_id` - Find events with user_id property
- `status:active` - Find only active events
- `team:growth` - Find events owned by growth team

## Organization Tips

### Event Naming Conventions

Follow consistent naming to make searching easier:
- Use verb-noun format: `view_product`, `click_button`
- Group related events: `signup_start`, `signup_complete`
- Be specific: `purchase_complete` vs `purchase_abandon`

### Use Descriptions Effectively

- Include searchable keywords in event descriptions
- Mention related features or user flows
- Note any special implementation requirements

### Maintain Status Accuracy

- Regularly update event statuses
- Archive old events instead of deleting them
- Use draft status during development

## Common Navigation Scenarios

### "I need to implement tracking for a login button"

1. Search for "login" events
2. Filter by status: "active"
3. Find the appropriate login event type
4. Review implementation examples
5. Check if similar elements already exist

### "I'm seeing inconsistent data for purchase events"

1. Search for "purchase" events
2. View all element instances
3. Compare property values across implementations
4. Check for missing required properties

### "I need to understand what events fire on the checkout page"

1. Navigate to checkout page in Canvas View
2. See all events mapped to that design
3. Review the event sequence and user flow
4. Validate that all critical actions are tracked

## Next Steps

Now that you can efficiently navigate your event schema, let's explore the [Figma Companion Plugin](figma-companion-plugin.md) to see how tracking integrates directly with your design workflow.