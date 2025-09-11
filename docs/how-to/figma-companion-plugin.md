# Figma Companion Plugin

Learn how to use Glazed's Figma plugin to seamlessly integrate analytics tracking with your design workflow.

## Overview

The Glazed Figma Companion Plugin bridges the gap between design and development by allowing you to view and interact with tracking specifications directly within Figma. This integration ensures that developers can see exactly what needs to be tracked without leaving their design reference.

## Prerequisites

Before using the Figma plugin, ensure you have:

- **Figma design file imported** into your Glazed project
- **Events linked to design elements** by your team
- **Plugin installed** from the Figma Community

## Installation

### From Figma Community

1. Open Figma and go to the Community tab
2. Search for "Glazed Analytics"
3. Click "Install" on the Glazed Companion Plugin
4. The plugin will be added to your Figma plugins

### From Glazed Dashboard

1. Navigate to your Glazed project
2. Go to Settings > Integrations
3. Click "Install Figma Plugin"
4. Follow the installation instructions

## Authentication and Setup

### Getting Your Figma Token

1. Log into your Glazed account
2. Go to Account Settings > API Tokens
3. Generate a new Figma Token
4. Copy the token for use in the plugin

### Connecting to Glazed

1. Open your Figma file
2. Launch the Glazed plugin from the Plugins menu

![Figma Plugin](images/figma-plugin-screenshot.png)
*Opening the Glazed Tracking Plan Companion plugin in Figma*
3. Enter your Figma Token when prompted
4. Select the matching Glazed project from the dropdown
5. Click "Connect" to establish the connection

## Using the Plugin

### Viewing Event Assignments

Once connected, the plugin will show:

- **Event indicators** on elements that have tracking assigned
- **Event names** and brief descriptions
- **Status badges** showing implementation state
- **Property previews** for quick reference

### Interactive Features

#### Selecting Elements

1. Click on any design element in Figma
2. The plugin automatically shows associated events
3. View complete event definitions without leaving Figma
4. See all properties and their expected values

#### Event Details Panel

When an element is selected, the plugin displays:

- **Event name** and description
- **All required properties** with types
- **Example implementation** code
- **Current status** (active, pending, etc.)
- **Implementation notes** from your team

#### Implementation Code

The plugin generates ready-to-use code snippets:

```javascript
// Example output for a purchase button
analytics.track('purchase_complete', {
  app_name: 'Glazed Store',
  product_id: 'ABC123',
  product_category: 'Electronics',
  price: 299.99,
  currency: 'USD'
});
```

### Navigation Features

#### Event List View

- See all events assigned to the current screen
- Filter by status or event type
- Quick navigation between different elements
- Overview of tracking coverage for the design

#### Search and Filter

- Search for specific events within the current file
- Filter by implementation status
- Find elements that need tracking attention
- Locate similar events for consistency

## Development Workflow

### During Implementation

1. **Open the design** in Figma alongside your code editor
2. **Launch the plugin** to see tracking requirements
3. **Select elements** as you implement their functionality
4. **Copy code snippets** directly from the plugin
5. **Mark as implemented** when complete

### Code Review Process

1. **Use plugin during reviews** to validate tracking coverage
2. **Check implementation examples** against actual code
3. **Verify all required properties** are included
4. **Ensure consistent naming** across similar events

### QA and Testing

1. **Reference plugin** during testing to understand expected behavior
2. **Validate event properties** match specifications
3. **Check edge cases** mentioned in implementation notes
4. **Verify tracking on all designed interactions**

## Advanced Features

### Multi-file Support

- Connect plugin to projects spanning multiple Figma files
- Maintain consistency across different design documents
- Track events across entire user journeys

### Team Collaboration

- See updates from designers and product managers in real-time
- Leave implementation notes directly in the plugin
- Track progress on event implementation across the team

### Integration with Development Tools

- Export tracking specifications for automated testing
- Generate implementation checklists
- Sync with project management tools

## Best Practices

### Organization

- **Use descriptive Figma layer names** to make element identification easier
- **Group related elements** for better plugin navigation
- **Maintain consistent design file structure** across projects

### Implementation

- **Always check the plugin** before implementing tracking
- **Use provided code snippets** as starting points
- **Validate against event definitions** in the plugin
- **Update status** when implementation is complete

### Team Workflow

- **Regularly sync** with designers about tracking requirements
- **Use plugin comments** for implementation questions
- **Share code examples** that work well with your tech stack
- **Review coverage** before feature releases

## Troubleshooting

### Connection Issues

- **Verify your Figma Token** is current and valid
- **Check project permissions** in Glazed
- **Ensure Figma file** matches imported project
- **Try refreshing** the plugin connection

### Missing Events

- **Confirm events are linked** in the Glazed web interface
- **Check layer selection** - plugin shows events for selected elements
- **Verify file sync** between Glazed and Figma
- **Look for nested elements** that might contain the events

### Performance

- **Close unused Figma files** to improve plugin performance
- **Refresh plugin connection** if data seems stale
- **Use smaller file sections** for complex designs
- **Clear plugin cache** if experiencing slowdowns

## Support and Resources

### Learning Resources

- **Video tutorials** available in the Glazed dashboard
- **Plugin documentation** in the Figma Community page
- **Example implementations** for common frameworks

### Getting Help

- **Slack channel**: Reach out for questions and bug reports
- **Support email**: Direct technical support from the Glazed team
- **Community forum**: Connect with other developers using Glazed

### Feature Requests

- **Submit feedback** through the plugin interface
- **Join beta testing** for new features
- **Contribute to roadmap** discussions

## Next Steps

Congratulations! You now have all the tools needed to effectively implement Glazed analytics in your applications. The combination of visual event mapping, clear tracking methodology, and seamless Figma integration gives you everything needed for accurate, maintainable analytics implementation.

Ready to start implementing? Return to your Glazed project dashboard to begin tracking your first events, or explore the [Getting Started guide](../getting-started/) if you need help setting up your initial project structure.