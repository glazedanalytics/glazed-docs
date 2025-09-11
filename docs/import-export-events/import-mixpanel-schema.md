# Import Mixpanel Schema into Glazed

Import your existing Mixpanel events and properties into Glazed to maintain consistency while adding visual design integration.

## Overview

The Mixpanel schema import allows you to bring your existing analytics setup into Glazed, preserving your event definitions while enabling visual mapping to design elements.

## Step-by-Step Guide

### Step 1: Open Mixpanel Project

1. Navigate to your **Mixpanel project**
2. Go to **Data Management**
3. Select **Lexicon**

![Mixpanel Icon](https://prod-files-secure.s3.us-west-2.amazonaws.com/706e5a16-a412-481d-97b8-98c8e9515846/10733b23-3f2f-42f2-9ef1-31e476dc7b35/Mixpanel_icon.png)

### Step 2: Access the Events Page

In the Lexicon section, you'll see all your defined events and their properties.

### Step 3: Export Your Schema

1. Click the **Export** button
2. This will open the export configuration dialog

### Step 4: Configure Export Settings

![Export Configuration](images/mixpanel-export-config.png)
*Mixpanel export configuration dialog*

1. Select **Type**: "Events & Properties"
2. Choose your preferred export format
3. Click **Send CSV**

The CSV file will contain:
- Event names
- Event descriptions  
- Property names and types
- Property descriptions
- Usage statistics

### Step 5: Upload to Glazed

![Glazed Upload Modal](images/glazed-upload-modal.png)
*Glazed tracking upload interface*

1. In your Glazed project, open the **Upload Tracking** modal
2. You can access this from:
   - Project Settings > Import
   - Main dashboard Import button
   - Tracking Schema section

### Step 6: Select Mixpanel as Source

![Mixpanel Source Selection](images/mixpanel-source-selection.png)
*Selecting Mixpanel as import source*

1. From the dropdown menu, select **Mixpanel**
2. This tells Glazed to use the Mixpanel-specific import parser
3. Click **Import** or **Upload File**

### Step 7: Upload CSV File

1. Select the CSV file you exported from Mixpanel
2. Click **Upload** to begin the import process
3. Glazed will parse and validate the schema

## What Gets Imported

### Events
- **Event Names**: Exact names from your Mixpanel setup
- **Event Descriptions**: Documentation from Mixpanel Lexicon
- **Event Status**: All imported as "Active" by default
- **Event Categories**: Preserved if defined in Mixpanel

### Properties
- **Property Names**: Exact property identifiers
- **Property Types**: Data types (string, number, boolean, etc.)
- **Property Descriptions**: Documentation from Lexicon
- **Required/Optional**: Based on Mixpanel property definitions

### Metadata
- **Creation Dates**: When events were first defined
- **Last Modified**: When properties were last updated
- **Usage Statistics**: Event volume data (if available)

## Post-Import Steps

### 1. Review Imported Events

After import, review all events in your Glazed project:

- **Verify event names** are correct
- **Check property definitions** match expectations
- **Update descriptions** if needed
- **Set event priorities** based on importance

### 2. Organize Events

Structure your imported events:

- **Create event categories** for better organization
- **Tag related events** for easier discovery
- **Set event statuses** (Active, Deprecated, etc.)
- **Add implementation notes** for developers

### 3. Map to Design Elements

The key advantage of Glazed is visual mapping:

- **Import your Figma designs** if not already done
- **Link events to design elements** where they should trigger
- **Configure element-specific properties** as needed
- **Review event coverage** across your user flows

### 4. Validate and Clean Up

Ensure data quality after import:

- **Remove duplicate events** if any were created
- **Merge similar events** that serve the same purpose
- **Update property types** if needed
- **Add missing event properties** discovered during review

## Common Import Issues

### Duplicate Events

**Issue**: Multiple events with similar names imported

**Solution**: 
- Review event names in Mixpanel before export
- Use Glazed's duplicate detection features
- Manually merge or remove duplicates after import

### Missing Properties

**Issue**: Some event properties not imported

**Solution**:
- Check Mixpanel export includes all properties
- Verify property visibility in Mixpanel Lexicon
- Add missing properties manually in Glazed

### Incorrect Data Types

**Issue**: Property types don't match expectations

**Solution**:
- Review data types in Mixpanel Lexicon
- Update property definitions in Glazed after import
- Use Glazed's property validation features

### Large Schema Size

**Issue**: Import takes long time or fails for large schemas

**Solution**:
- Export smaller subsets of events if possible
- Remove unused events from Mixpanel before export
- Contact support for assistance with large imports

## Best Practices

### Before Import

- **Audit your Mixpanel schema** to remove unused events
- **Clean up event names** and descriptions
- **Ensure property definitions** are accurate and complete
- **Document any custom implementation** notes

### During Import

- **Use descriptive import names** to track different versions
- **Import in smaller batches** if you have many events
- **Verify each import step** before proceeding
- **Keep the original CSV** as backup

### After Import

- **Map high-priority events first** to design elements
- **Create implementation documentation** for developers  
- **Set up validation rules** for event properties
- **Plan regular schema updates** as events evolve

## Integration Benefits

### Consistency
- **Maintain existing event names** developers are familiar with
- **Preserve property definitions** to avoid implementation changes
- **Keep historical context** from Mixpanel documentation

### Enhancement
- **Add visual context** by linking to design elements
- **Improve developer experience** with clear element mapping
- **Enable design-driven analytics** workflow
- **Create better documentation** through visual association

### Migration Path
- **Gradual transition** from Mixpanel-only to Glazed-enhanced workflow
- **Maintain backward compatibility** with existing tracking code
- **Prepare for future platform migrations** with portable schema

## Troubleshooting

### Export Issues from Mixpanel

- Ensure you have **admin access** to the Mixpanel project
- Check that **events exist** in the Lexicon
- Verify **export permissions** for your account
- Try exporting **smaller date ranges** if timeout occurs

### Import Issues in Glazed

- Verify **CSV format** matches Mixpanel export structure
- Check for **special characters** in event names that might cause issues
- Ensure **file size limits** are not exceeded
- Contact support if **parsing errors** occur

## Next Steps

After successfully importing your Mixpanel schema:

1. **Review the imported events** in your Glazed project
2. **Start mapping events to design elements** in your Figma files
3. **Create implementation guides** for your development team
4. **Set up data validation** with your existing Mixpanel implementation

Need help with the import process? Join our [Slack community](https://join.slack.com/t/glazedanalytics/shared_invite/zt-27kt7tl3n-lkfs1mzqCzyVSKdkiQx2sA) or contact [hello@glazedanalytics.com](mailto:hello@glazedanalytics.com) for assistance.