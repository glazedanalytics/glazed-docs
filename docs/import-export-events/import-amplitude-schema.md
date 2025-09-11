# Import Amplitude Schema into Glazed

Import your existing Amplitude events and properties into Glazed to enhance your analytics workflow with visual design integration.

## Overview

The Amplitude schema import enables you to bring your existing analytics implementation into Glazed, maintaining your event structure while adding powerful visual mapping capabilities to design elements.

## Step-by-Step Guide

### Step 1: Open Amplitude Project

1. Navigate to your **Amplitude project**
2. Go to **Data** > **Events**

![Amplitude Navigation](https://prod-files-secure.s3.us-west-2.amazonaws.com/706e5a16-a412-481d-97b8-98c8e9515846/fc10764b-3e1b-444e-a877-84ab659e01c1/Frame_142.png)
*Navigate to Data > Events in your Amplitude project*

### Step 2: Access Schema Download

In the Events section, you'll see all your tracked events with their properties and statistics.

### Step 3: Download Events Schema

![Download Button](https://prod-files-secure.s3.us-west-2.amazonaws.com/706e5a16-a412-481d-97b8-98c8e9515846/657d6cd1-4cec-48e9-a490-4c5378a6878d/Frame_143.png)
*Click the download button to export your schema*

1. Look for the **download (⬇️) button** in the Events interface
2. Click the download button to open export options

### Step 4: Select Schema Type

![Schema Selection](images/amplitude-schema-selection.png)
*Select the complete schema export option*

1. Choose **"Schema of all Events and their Event Properties"**
2. This ensures you get the complete event definitions
3. Click **Download**

The downloaded file will include:
- All event names and descriptions
- Event properties with data types
- Property descriptions and constraints
- Validation rules and formatting

### Step 5: Upload to Glazed

![Glazed Upload Interface](https://prod-files-secure.s3.us-west-2.amazonaws.com/706e5a16-a412-481d-97b8-98c8e9515846/a5fcb8d9-7e7d-45d3-9802-ddc180c518ac/Screenshot_2024-04-19_at_14.00.47.png)
*Glazed tracking upload interface*

1. In your Glazed project, open the **Upload Tracking** modal
2. Access this from:
   - Project Settings > Import Events
   - Dashboard Import button
   - Tracking Schema management section

### Step 6: Select Amplitude as Source

![Amplitude Source Selection](https://prod-files-secure.s3.us-west-2.amazonaws.com/706e5a16-a412-481d-97b8-98c8e9515846/14ecb662-a6ee-4da6-aa2a-9f3b552f5bc9/bbca64e5-24fc-4f2b-bfa6-72fad6845dbc.png)
*Select Amplitude from the import source options*

1. From the source dropdown menu, select **Amplitude**
2. This configures Glazed to use the Amplitude-specific parser
3. The interface will adapt to Amplitude's schema format

### Step 7: Complete Import

1. **Upload the CSV file** you downloaded from Amplitude
2. **Review the import preview** to verify events are parsed correctly
3. **Click Import** to complete the process
4. **Wait for processing** - large schemas may take a few minutes

## What Gets Imported

### Event Information
- **Event Names**: Exact event identifiers from Amplitude
- **Event Descriptions**: Documentation and context from Amplitude
- **Event Volume**: Usage statistics and frequency data
- **Event Status**: All imported as "Active" initially

### Property Details
- **Property Names**: Complete property identifiers
- **Data Types**: String, number, boolean, array, object types
- **Property Descriptions**: Documentation from Amplitude
- **Validation Rules**: Constraints and formatting requirements
- **Example Values**: Sample data when available

### Metadata
- **Schema Version**: Timestamp of when schema was exported
- **Project Context**: Source project information
- **Custom Properties**: User-defined properties and tags

## Post-Import Workflow

### 1. Validate Imported Data

Review the imported schema for accuracy:

- **Check event completeness** - Ensure all expected events imported
- **Verify property definitions** - Confirm data types and descriptions
- **Review event relationships** - Check for event hierarchies or groupings
- **Validate custom properties** - Ensure user-defined properties imported correctly

### 2. Organize Your Schema

Structure the imported events for better management:

- **Create event categories** based on user journeys or features
- **Add event tags** for filtering and discovery
- **Set priority levels** for implementation focus
- **Update descriptions** with implementation context

### 3. Map Events to Design

Connect your analytics to visual elements:

- **Import or link Figma designs** to your Glazed project
- **Map events to specific UI elements** where they should trigger
- **Configure element-level properties** for contextual tracking
- **Review coverage** across your complete user experience

### 4. Enhance Event Definitions

Improve upon the imported schema:

- **Add implementation notes** for developers
- **Create event groupings** for related actions
- **Define event relationships** and dependencies
- **Set up validation rules** for data quality

## Advanced Import Options

### Selective Import

If you have a large Amplitude schema:

1. **Filter events by date range** in Amplitude before export
2. **Export specific event categories** separately
3. **Import in batches** for better control and review
4. **Combine imports** in Glazed after individual validation

### Custom Property Mapping

For complex property structures:

1. **Review property nesting** in Amplitude export
2. **Map nested properties** to flat structure if needed
3. **Configure data type transformations** in Glazed
4. **Set up property validation** rules after import

## Common Import Scenarios

### Migration from Amplitude to Glazed

**Use Case**: Moving analytics workflow to Glazed while maintaining existing events

**Approach**:
1. Import complete Amplitude schema
2. Gradually map events to design elements
3. Maintain parallel tracking during transition
4. Phase out direct Amplitude dependency

### Adding Design Context to Existing Analytics

**Use Case**: Enhancing current Amplitude setup with visual mapping

**Approach**:
1. Import existing schema to preserve definitions
2. Link events to Figma design elements
3. Use Glazed for new feature development
4. Maintain Amplitude for historical data analysis

### Team Collaboration Enhancement

**Use Case**: Improving collaboration between design, product, and engineering

**Approach**:
1. Import shared event definitions from Amplitude
2. Create visual documentation through design mapping
3. Use Glazed as single source of truth for new events
4. Export enhanced specifications for implementation

## Troubleshooting

### Export Issues from Amplitude

**Problem**: Unable to download schema from Amplitude

**Solutions**:
- Verify you have **admin or analyst permissions**
- Check that **events exist** in the specified time range
- Try **smaller date ranges** if export times out
- Ensure your **Amplitude plan** supports schema export

**Problem**: Downloaded file is empty or incomplete

**Solutions**:
- Verify events exist in the selected date range
- Check **event visibility settings** in Amplitude
- Try exporting **"All Events"** instead of filtered views
- Contact Amplitude support for export issues

### Import Issues in Glazed

**Problem**: Import fails or shows parsing errors

**Solutions**:
- Verify the **CSV format** matches Amplitude export structure
- Check for **special characters** in event names that may cause issues
- Ensure **file encoding** is UTF-8
- Try importing **smaller batches** if file is very large

**Problem**: Missing events or properties after import

**Solutions**:
- Review **original Amplitude export** for completeness
- Check **import logs** in Glazed for any warnings
- Verify **property visibility** in Amplitude before export
- Manually add **missing definitions** in Glazed after import

### Data Quality Issues

**Problem**: Incorrect property types or descriptions

**Solutions**:
- **Update property definitions** in Glazed after import
- **Add validation rules** to catch data type mismatches
- **Review event documentation** for accuracy
- **Set up monitoring** for ongoing data quality

## Best Practices

### Pre-Import Preparation

- **Clean up unused events** in Amplitude before export
- **Update event descriptions** to be clear and complete
- **Review property definitions** for accuracy
- **Document any custom implementation** details

### During Import

- **Import in smaller batches** for large schemas
- **Validate each step** before proceeding
- **Keep original export files** as backup
- **Document import settings** used

### Post-Import Optimization

- **Review and organize** imported events immediately
- **Start with high-priority events** for design mapping
- **Create developer documentation** based on enhanced schema
- **Set up regular schema updates** process

## Integration Benefits

### Enhanced Developer Experience

- **Visual context** for event implementation
- **Clear element mapping** reduces guesswork  
- **Comprehensive documentation** in one place
- **Validation tools** for implementation accuracy

### Improved Team Collaboration

- **Shared visual language** between teams
- **Design-driven analytics** approach
- **Centralized event documentation**
- **Cross-functional alignment** on tracking goals

### Better Analytics Workflow

- **Proactive event planning** during design phase
- **Consistent implementation** across features
- **Easier maintenance** and updates
- **Quality assurance** through validation

## Next Steps

After successfully importing your Amplitude schema:

1. **Review imported events** for completeness and accuracy
2. **Begin mapping high-priority events** to design elements
3. **Create implementation guides** for your development team
4. **Set up validation workflows** to maintain data quality
5. **Plan transition strategy** if moving away from direct Amplitude tracking

Ready to enhance your analytics workflow? Start mapping your imported events to design elements, or reach out to our [support team](mailto:hello@glazedanalytics.com) for guidance on optimizing your Glazed setup.