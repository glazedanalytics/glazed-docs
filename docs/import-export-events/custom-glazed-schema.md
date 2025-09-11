# Custom Glazed Schema

Create and import custom event schemas using Glazed's native format for maximum flexibility and control.

## Overview

The Custom Glazed Schema format provides the most comprehensive way to define your analytics events, offering full control over event properties, validation rules, and implementation specifications.

## Glazed Schema Format

### JSON Structure

The native Glazed schema uses JSON format with the following structure:

```json
{
  "schema_version": "1.0",
  "project": {
    "name": "Your Project Name",
    "description": "Project description",
    "created_at": "2024-01-01T00:00:00Z"
  },
  "events": [
    {
      "name": "event_name",
      "display_name": "Event Display Name",
      "description": "Event description",
      "category": "user_interaction",
      "status": "active",
      "properties": [
        {
          "name": "property_name",
          "display_name": "Property Display Name",
          "description": "Property description",
          "type": "string",
          "required": true,
          "default_value": null,
          "validation_rules": {
            "max_length": 255,
            "allowed_values": ["option1", "option2"]
          }
        }
      ],
      "implementation": {
        "platforms": ["web", "mobile", "server"],
        "code_examples": {
          "javascript": "analytics.track('event_name', { property_name: 'value' });",
          "python": "analytics.track('event_name', { 'property_name': 'value' })"
        }
      }
    }
  ]
}
```

### Schema Components

#### Project Metadata
- **schema_version**: Version of the Glazed schema format
- **project**: Basic project information and metadata
- **name**: Human-readable project name
- **description**: Project purpose and context
- **created_at**: ISO timestamp of schema creation

#### Event Definitions
- **name**: Technical event identifier (snake_case recommended)
- **display_name**: Human-readable event name
- **description**: Detailed event description and context
- **category**: Event grouping (e.g., "user_interaction", "system", "business")
- **status**: Event lifecycle status ("active", "deprecated", "draft")

#### Property Specifications
- **name**: Technical property identifier
- **display_name**: Human-readable property name
- **description**: Property purpose and usage
- **type**: Data type ("string", "number", "boolean", "array", "object")
- **required**: Whether property is mandatory
- **default_value**: Default value if not provided
- **validation_rules**: Constraints and validation logic

#### Implementation Details
- **platforms**: Supported platforms for the event
- **code_examples**: Implementation examples in different languages

## Creating Custom Schemas

### Method 1: Export and Modify

1. **Export existing schema** from your Glazed project
2. **Modify the JSON** to add new events or properties
3. **Validate structure** using JSON schema validator
4. **Import modified schema** back into Glazed

### Method 2: Build from Template

Start with our schema template:

```json
{
  "schema_version": "1.0",
  "project": {
    "name": "My Custom Analytics Project",
    "description": "Custom event schema for my application"
  },
  "events": [
    {
      "name": "user_signup",
      "display_name": "User Signup",
      "description": "User creates a new account",
      "category": "conversion",
      "status": "active",
      "properties": [
        {
          "name": "signup_method",
          "display_name": "Signup Method",
          "description": "How the user signed up",
          "type": "string",
          "required": true,
          "validation_rules": {
            "allowed_values": ["email", "google", "facebook", "apple"]
          }
        },
        {
          "name": "user_type",
          "display_name": "User Type",
          "description": "Type of user account",
          "type": "string",
          "required": false,
          "default_value": "free"
        }
      ]
    }
  ]
}
```

### Method 3: Generate Programmatically

Use code to generate schemas for complex projects:

```javascript
// Example: Generate schema from existing tracking code
const generateGlazedSchema = (trackingCalls) => {
  const schema = {
    schema_version: "1.0",
    project: {
      name: "Generated Schema",
      description: "Auto-generated from existing tracking"
    },
    events: []
  };

  // Parse tracking calls and generate event definitions
  trackingCalls.forEach(call => {
    const event = {
      name: call.eventName,
      display_name: formatDisplayName(call.eventName),
      description: call.description || "",
      category: inferCategory(call.eventName),
      status: "active",
      properties: generateProperties(call.properties)
    };
    schema.events.push(event);
  });

  return schema;
};
```

## Advanced Schema Features

### Event Relationships

Define relationships between events:

```json
{
  "name": "purchase_complete",
  "relationships": {
    "triggers_after": ["add_to_cart", "checkout_start"],
    "triggers_before": ["purchase_success_page_view"],
    "mutually_exclusive": ["purchase_cancelled"]
  }
}
```

### Conditional Properties

Properties that only apply under certain conditions:

```json
{
  "name": "discount_amount",
  "type": "number",
  "required": false,
  "conditional_logic": {
    "required_when": {
      "property": "has_discount",
      "equals": true
    }
  }
}
```

### Platform-Specific Configurations

Different configurations for different platforms:

```json
{
  "name": "page_view",
  "platform_configs": {
    "web": {
      "properties": ["url", "referrer", "user_agent"]
    },
    "mobile": {
      "properties": ["screen_name", "app_version", "device_type"]
    }
  }
}
```

### Custom Validation Rules

Advanced validation for property values:

```json
{
  "validation_rules": {
    "type": "string",
    "pattern": "^[A-Z]{2}$",
    "description": "Two-letter country code"
  }
}
```

## Import Process

### Step 1: Prepare Schema File

1. **Create or modify** your JSON schema file
2. **Validate JSON syntax** using a JSON validator
3. **Check schema structure** against Glazed specifications
4. **Test with sample data** if possible

### Step 2: Import to Glazed

1. **Open Glazed project**
2. **Navigate to Import** section
3. **Select "Custom Schema"** as import type
4. **Upload JSON file**
5. **Review import preview**
6. **Confirm import**

### Step 3: Validate Import

1. **Review imported events** for completeness
2. **Check property definitions** are correct
3. **Verify validation rules** are working
4. **Test event creation** with sample data

## Schema Validation

### JSON Schema Validation

Validate your custom schema against our JSON Schema:

```bash
# Using a JSON schema validator
jsonschema -i your-schema.json glazed-schema.json
```

### Common Validation Errors

**Invalid event names**
```json
// ❌ Invalid - contains spaces and special characters
"name": "User Sign-Up!"

// ✅ Valid - snake_case format
"name": "user_signup"
```

**Missing required fields**
```json
// ❌ Invalid - missing required fields
{
  "name": "click_button"
  // Missing: display_name, description, properties
}

// ✅ Valid - all required fields present
{
  "name": "click_button",
  "display_name": "Button Click",
  "description": "User clicks a button",
  "properties": []
}
```

**Invalid property types**
```json
// ❌ Invalid - unsupported type
{
  "name": "timestamp",
  "type": "datetime"
}

// ✅ Valid - supported type
{
  "name": "timestamp",
  "type": "string",
  "validation_rules": {
    "format": "iso8601"
  }
}
```

## Export and Backup

### Project-Level Export

Export your complete schema for backup or sharing:

1. **Go to Project Settings** > Export
2. **Select "Complete Schema"**
3. **Choose JSON format**
4. **Download file**

### Version Control

Maintain schema versions:

```json
{
  "schema_version": "1.2",
  "project": {
    "name": "My Project",
    "version": "v2.1.0",
    "last_modified": "2024-01-15T10:30:00Z"
  }
}
```

## Best Practices

### Schema Design

- **Use consistent naming** conventions (snake_case for technical names)
- **Include comprehensive descriptions** for all events and properties
- **Define validation rules** to ensure data quality
- **Group related events** with categories
- **Plan for future changes** with extensible property design

### Event Definition

- **Be specific** with event names and descriptions
- **Include business context** in descriptions
- **Define clear property purposes**
- **Set appropriate required/optional flags**
- **Add implementation examples**

### Property Configuration

- **Choose appropriate data types**
- **Set realistic validation constraints**
- **Provide default values** where sensible
- **Document expected value formats**
- **Consider null value handling**

### Schema Management

- **Version your schemas** for change tracking
- **Backup before major changes**
- **Test imports in staging** environments
- **Document schema changes**
- **Coordinate with development teams**

## Integration Examples

### E-commerce Schema

```json
{
  "events": [
    {
      "name": "product_view",
      "category": "product_interaction",
      "properties": [
        {
          "name": "product_id",
          "type": "string",
          "required": true
        },
        {
          "name": "product_price",
          "type": "number",
          "validation_rules": {
            "minimum": 0
          }
        }
      ]
    }
  ]
}
```

### SaaS Application Schema

```json
{
  "events": [
    {
      "name": "feature_used",
      "category": "feature_interaction",
      "properties": [
        {
          "name": "feature_name",
          "type": "string",
          "required": true
        },
        {
          "name": "user_plan",
          "type": "string",
          "validation_rules": {
            "allowed_values": ["free", "pro", "enterprise"]
          }
        }
      ]
    }
  ]
}
```

## Troubleshooting

### Import Failures

**JSON syntax errors**
- Use a JSON validator to check syntax
- Common issues: trailing commas, unescaped quotes
- Validate with online JSON validators

**Schema validation errors**
- Check required fields are present
- Verify data types are supported
- Ensure naming conventions are followed

**Large file issues**
- Break large schemas into smaller files
- Import in batches by category
- Contact support for very large schemas

## Support and Resources

- **JSON Schema Documentation**: Complete reference for schema structure
- **Example Templates**: Pre-built schemas for common use cases
- **Validation Tools**: Online validators and testing utilities
- **Community Support**: [Slack community](https://join.slack.com/t/glazedanalytics/shared_invite/zt-27kt7tl3n-lkfs1mzqCzyVSKdkiQx2sA) for help and tips

Ready to create your custom schema? Start with our template and build the perfect analytics specification for your project.