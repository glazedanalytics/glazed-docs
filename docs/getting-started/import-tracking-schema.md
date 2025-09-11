# Import Tracking Schema into Glazed

Connect your existing analytics events to Glazed by importing your tracking schema from platforms like Mixpanel or Amplitude.

## Video Tutorial

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%;">
  <iframe src="https://www.youtube.com/embed/UG74Urf3Seg" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
</div>

## Prerequisites

- **Access to your analytics project** (Mixpanel, Amplitude, or similar)
- Your existing event tracking schema or event definitions

## Import from Analytics Platforms

### 1. Download Your Schema

#### From Mixpanel:
1. Navigate to your Mixpanel project
2. Go to Data Management > Events
3. Export your event schema/definitions

#### From Amplitude:
1. Access your Amplitude project
2. Go to Data > Events
3. Download your event schema

#### Other Platforms:
Most analytics platforms provide export functionality for event schemas. Look for:
- Event definitions
- Event properties
- Event taxonomy exports

### 2. Upload to Glazed

1. In your Glazed project, navigate to "Import Schema"
2. Select "Upload from Analytics Platform"
3. Choose your downloaded schema file
4. Review and confirm the import

## Alternative: Glazed Template Spreadsheet

If you don't have an existing schema or want to start fresh:

### 1. Download Template

1. In Glazed, select "Use Template Spreadsheet"
2. Download the Glazed event template
3. The template includes standard e-commerce and SaaS events

### 2. Customize Your Events

1. Open the spreadsheet template
2. Add your specific events and properties
3. Follow the template format for consistency
4. Save your customized spreadsheet

### 3. Upload to Glazed

1. Return to Glazed
2. Upload your customized spreadsheet
3. Review the imported events

## Schema Structure

Your imported schema should include:

- **Event Names**: Clear, descriptive event identifiers
- **Event Properties**: Parameters specific to each event
- **User Properties**: Attributes that describe your users
- **Event Descriptions**: Context for when events should fire

## Best Practices

### Event Naming

- Use consistent naming conventions
- Be descriptive but concise
- Group related events with prefixes (e.g., `signup_`, `purchase_`)

### Property Definition

- Define clear data types for each property
- Include example values
- Document required vs. optional properties

## Validation

After importing, Glazed will:

- Validate your schema format
- Check for naming conflicts
- Highlight any missing required fields
- Suggest improvements for consistency

## Next Steps

With your schema imported, you can now [Link Events to Design Elements](link-events-to-design.md) to start mapping your tracking implementation.