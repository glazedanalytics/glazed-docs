# Create Event Properties and User Properties

Define the data structure for your events by creating properties that will be tracked with each user interaction.

## Overview

Properties are the key-value pairs that provide context and detail for your events. There are two main types:

- **Event Properties**: Data specific to a particular event instance
- **User Properties**: Attributes that describe the user performing the event

## Event Properties

### Creating Event Properties

1. Navigate to your event in the Glazed interface
2. Click "Add Property" in the Event Properties section
3. Define the property details:
   - **Name**: Clear, descriptive identifier
   - **Type**: String, Number, Boolean, Date, etc.
   - **Description**: Context for when/how this property is used
   - **Required**: Whether this property must always be present

### Common Event Properties

#### E-commerce Events
- `product_id`: Unique identifier for products
- `product_category`: Category classification
- `price`: Product or transaction value
- `quantity`: Number of items
- `discount_applied`: Whether a discount was used

#### Navigation Events
- `page_name`: Current page identifier
- `section`: Area of the application
- `previous_page`: Where the user came from
- `navigation_method`: How they navigated (menu, search, direct)

#### Form Events
- `form_name`: Identifier for the form
- `field_name`: Specific field being interacted with
- `form_step`: For multi-step forms
- `validation_errors`: Any errors encountered

### Event Statuses

Define different states for your events:

- **Active**: Currently being tracked
- **Deprecated**: Still firing but being phased out
- **Draft**: In development, not yet implemented
- **Archived**: No longer in use

## User Properties

### Creating User Properties

1. Go to User Properties in your Glazed project
2. Click "Add User Property"
3. Define the property:
   - **Name**: User attribute identifier
   - **Type**: Data type of the property
   - **Description**: What this attribute represents
   - **Update Frequency**: How often this property changes

### Common User Properties

#### Identity Properties
- `user_id`: Unique user identifier
- `email`: User email address
- `username`: Display name or handle
- `account_type`: Free, premium, enterprise, etc.

#### Demographic Properties
- `age_group`: Age range categories
- `location`: Geographic information
- `signup_date`: When they joined
- `subscription_tier`: Service level

#### Behavioral Properties
- `total_purchases`: Lifetime purchase count
- `last_active_date`: Most recent activity
- `feature_flags`: Enabled features or experiments
- `preferred_language`: Language setting

## Property Assignment

### Assigning to Events

1. Select an event from your schema
2. In the Properties section, choose relevant properties
3. Set default values where appropriate
4. Mark required vs. optional properties

### Assigning to Elements

When linking events to design elements:

1. Select the design element
2. Choose the assigned event
3. Configure element-specific property values
4. Override defaults where necessary

## Best Practices

### Naming Conventions

- **Use snake_case**: Consistent formatting (e.g., `user_id`, `product_name`)
- **Be descriptive**: Clear what the property represents
- **Avoid abbreviations**: Unless they're industry standard
- **Group related properties**: Use prefixes for organization

### Data Types

- **Choose appropriate types**: String, Number, Boolean, Date
- **Consider constraints**: Min/max values, allowed strings
- **Plan for null values**: How to handle missing data
- **Think about analytics**: What analysis will you perform?

### Organization

- **Group by context**: Organize properties by feature or flow
- **Document relationships**: How properties relate to each other
- **Maintain consistency**: Same property names across similar events
- **Regular cleanup**: Remove unused or duplicate properties

## Advanced Configuration

### Conditional Properties

Some properties may only apply in certain contexts:

- Set conditions for when properties should be collected
- Define fallback values for missing data
- Create calculated properties based on other values

### Property Validation

Ensure data quality by setting:

- **Required properties**: Must be present for the event to be valid
- **Format validation**: Regex patterns for strings, ranges for numbers
- **Enum values**: Restricted lists of allowed values

## Implementation Notes

### For Developers

Your property definitions in Glazed will become:

- **Schema documentation**: Clear specifications for implementation
- **Validation rules**: Automated checking of event data
- **Type definitions**: Strong typing for development
- **Testing criteria**: What to verify in QA

### For Analysts

Well-defined properties enable:

- **Consistent reporting**: Same definitions across all analysis
- **Automated dashboards**: Reliable data structure
- **Advanced segmentation**: Rich user and event attributes
- **Cohort analysis**: User property-based groupings

## Quality Assurance

### Review Checklist

- [ ] All critical user journeys have appropriate events and properties
- [ ] Property names follow consistent conventions
- [ ] Required vs. optional properties are clearly marked
- [ ] Data types are appropriate for planned analysis
- [ ] Descriptions are clear and comprehensive

### Testing Your Schema

Before implementation:

1. **Walkthrough user flows**: Ensure all interactions are captured
2. **Validate property logic**: Check that properties make sense together
3. **Review with stakeholders**: Get input from analysts and product team
4. **Consider edge cases**: How will you handle unusual scenarios?

## Next Steps

With your properties defined, you're ready to:

- Export your tracking specification for development
- Begin implementation in your application
- Set up monitoring and validation
- Create dashboards and analysis based on your schema

Your Glazed project now contains a complete, visual tracking plan that bridges design and analytics!