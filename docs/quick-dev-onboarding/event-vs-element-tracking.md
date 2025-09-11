# Event vs Element Level Tracking

Master Glazed's unique two-level tracking approach that provides both consistency and flexibility.

## Overview

Glazed introduces a sophisticated tracking methodology with two distinct levels:
- **Event Level**: The canonical definition and source of truth
- **Element Level**: Specific instances with contextual variations

This approach ensures consistency while allowing for the flexibility needed in real-world applications.

![Event vs Element Level Tracking](images/event-vs-element-comparison.png)
*Visual comparison of Event Level and Element Level tracking perspectives*

## Event Level Tracking

The Event Level contains the complete definition for a specific event type. It serves as the "source of truth" for how that event should be implemented across your entire application.

### Event Level Properties

An event level definition includes:
- **Event Name**: The canonical identifier (e.g., `login`, `purchase`, `signup`)
- **Event Properties**: All possible properties this event can have
- **Property Types**: Data types and validation rules
- **Descriptions**: Context for when and why this event fires

### Example: Login Event

```javascript
// Event Level Definition
Event: "login"
Properties:
- app_name (string, required): The name of the application
- login_method (string, required): How the user logged in
- user_type (string, optional): Type of user account
- timestamp (date, auto): When the login occurred
```

## Element Level Tracking

The Element Level represents specific instances of an event with contextual property values. Each UI element that triggers the same event type can have different property values based on its context.

### Element Level Implementation

Using the login event example, different login buttons would implement the same event with different property values:

```javascript
// Native login button (Element Level Instance 1)
analytics.track('login', {
  app_name: 'Glazed App',
  login_method: 'Native',
  user_type: 'premium'
});

// Google login button (Element Level Instance 2)
analytics.track('login', {
  app_name: 'Glazed App',
  login_method: 'Google',
  user_type: 'free'
});

// Facebook login button (Element Level Instance 3)
analytics.track('login', {
  app_name: 'Glazed App',
  login_method: 'Facebook',
  user_type: 'free'
});
```

![Tracking Implementation Example](images/tracking-pseudocode.png)
*Example of how tracking methods are implemented in practice*

## Benefits of This Approach

### Consistency
- All instances of an event share the same structure
- Property names and types are standardized
- Easy to aggregate data across different contexts

### Flexibility
- Each element can provide contextually appropriate values
- Support for conditional properties based on element context
- Accommodate different user flows while maintaining structure

### Maintainability
- Change event structure in one place, update everywhere
- Clear separation between definition and implementation
- Easy to audit and validate tracking implementation

## Working with Both Levels

### As a Developer

1. **Start with Event Level**: Understand the canonical event definition
2. **Implement Element Level**: Use the definition to implement specific instances
3. **Validate Consistency**: Ensure all instances conform to the event structure

### Event Definition Process

```javascript
// 1. Define the event at the Event Level
const loginEventDefinition = {
  name: 'login',
  properties: {
    app_name: { type: 'string', required: true },
    login_method: { type: 'string', required: true },
    user_type: { type: 'string', required: false }
  }
};

// 2. Implement specific instances at Element Level
function trackNativeLogin() {
  analytics.track('login', {
    app_name: 'Glazed App',
    login_method: 'Native',
    user_type: getCurrentUserType()
  });
}

function trackGoogleLogin() {
  analytics.track('login', {
    app_name: 'Glazed App',
    login_method: 'Google',
    user_type: 'free'
  });
}
```

## Advanced Concepts

### Property Inheritance
Element Level instances can:
- Override default values from Event Level
- Add element-specific properties (if allowed)
- Omit optional properties when not applicable

### Conditional Properties
Some properties may only apply in certain contexts:

```javascript
// E-commerce purchase event
analytics.track('purchase', {
  app_name: 'Glazed Store',
  product_id: 'ABC123',
  price: 29.99,
  // Discount code only included if applicable
  ...(discountCode && { discount_code: discountCode })
});
```

![Backend Events View](images/backend-events.png)  
*Backend event tracking and validation in Glazed*

### Validation
Glazed automatically validates that Element Level implementations conform to Event Level definitions, catching errors before they reach production.

## Best Practices

### Event Level Design
- Keep event names descriptive but concise
- Define all possible properties upfront
- Use consistent naming conventions
- Document the business purpose of each event

### Element Level Implementation
- Always reference the Event Level definition
- Provide all required properties
- Use consistent property values across similar elements
- Include meaningful contextual information

### Team Collaboration
- Product teams define Event Level requirements
- Design teams map events to interface elements
- Development teams implement Element Level instances
- All teams use Glazed as the single source of truth

## Next Steps

Now that you understand Glazed's tracking methodology, let's learn how to [Find and Navigate Events](finding-and-navigating-events.md) efficiently in the Glazed interface.