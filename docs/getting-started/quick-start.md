# Quick Start

Get up and running with Glazed in under 10 minutes. This guide will walk you through the essential steps to create your first visual tracking plan.

## What You'll Accomplish

By the end of this quick start, you'll have:
- ✅ Connected your Figma design to Glazed
- ✅ Imported your existing analytics events (or created new ones)
- ✅ Linked events to specific design elements
- ✅ Generated implementation-ready tracking specifications

**Estimated time**: 8-10 minutes

## Prerequisites

Before you begin, make sure you have:
- **Figma account** with a design file you want to track
- **Glazed account** (sign up at [glazedanalytics.com](https://glazedanalytics.com))
- **Read access** to the Figma file you want to import
- **Existing analytics setup** (Mixpanel, Amplitude) or willingness to start fresh

## Step 1: Create Your Glazed Project (1 minute)

1. **Log into Glazed** at [app.glazedanalytics.com](https://app.glazedanalytics.com)
2. **Click "New Project"**
3. **Name your project** (e.g., "Mobile App Tracking", "Website Analytics")
4. **Select your team** if you're part of multiple teams
5. **Click "Create Project"**

## Step 2: Import Your Figma Design (2 minutes)

1. **Open your Figma file** in a new browser tab
2. **Copy the Figma file URL** from your browser address bar
3. **Return to Glazed** and click "Import Figma File"
4. **Paste the URL** and ensure you have proper sharing permissions enabled:
   - Enable "Viewers can copy, save, and export" in Figma share settings
5. **Click "Import"** and wait for processing (usually 30-60 seconds)

> **💡 Tip**: For best performance, start with files that have fewer than 100 screens

## Step 3: Set Up Your Event Schema (2-3 minutes)

Choose one of these options based on your current analytics setup:

### Option A: Import Existing Events (Recommended)

If you're already using Mixpanel or Amplitude:

**For Mixpanel Users:**
1. In Mixpanel: Go to **Data Management** > **Lexicon**
2. Click **Export** and select "Events & Properties"
3. **Download the CSV**
4. In Glazed: **Upload Tracking** > Select **Mixpanel** > Import your CSV

**For Amplitude Users:**
1. In Amplitude: Go to **Data** > **Events**  
2. Click the **download button (⬇️)**
3. Select **"Schema of all Events and their Event Properties"**
4. In Glazed: **Upload Tracking** > Select **Amplitude** > Import your CSV

### Option B: Start Fresh with AI Suggestions

If you're new to analytics or want to start over:
1. **Skip the import step** for now
2. Glazed's AI will **suggest relevant events** when you start mapping to design elements
3. **Accept or customize** the AI suggestions based on your needs

## Step 4: Link Events to Design Elements (3-4 minutes)

This is where the magic happens - connecting your analytics to your visual designs:

1. **Navigate to your imported Figma file** in Glazed
2. **Browse to a key screen** (e.g., login, signup, checkout)
3. **Click on interactive elements** like buttons, forms, and links
4. **Assign events** to each element:
   - **Use existing events** from your import, or
   - **Create new events** with AI suggestions
5. **Configure element-specific properties** (e.g., button_name: "Login")

### Priority Elements to Track
Focus on these high-impact elements first:
- **Conversion buttons** (Sign up, Purchase, Subscribe)
- **Navigation elements** (Menu items, page links)
- **Form interactions** (Input focus, form submission)
- **Feature usage** (Tool usage, content interaction)

## Step 5: Generate Implementation Specs (1 minute)

1. **Review your event mapping** to ensure completeness
2. **Export your tracking plan**:
   - **Page-level export**: For specific screens (JSON or CSV)
   - **Project-level export**: For complete implementation (JSON or CSV)
3. **Download the specifications** for your development team

## Step 6: Install the Figma Plugin (Optional, 1 minute)

Enhance your workflow with our Figma companion:

1. **Search "Glazed"** in Figma Community plugins
2. **Install the plugin** to your Figma account
3. **Launch from your Figma file** to see events in context
4. **Copy implementation code** directly from the plugin

## What's Next?

### For Your Development Team
- **Share the exported specifications** with clear implementation requirements
- **Use the Figma plugin** during development for visual context
- **Implement tracking** using the provided code examples
- **Validate implementation** against Glazed specifications

### Expand Your Tracking
- **Add more screens** from your Figma file
- **Create event categories** for better organization  
- **Set up data validation** with datawarehouse connectors
- **Collaborate with your team** on tracking requirements

### Advanced Features
- **Set up datawarehouse validation** ([BigQuery](../datawarehouse-connectors/bigquery-connector.md), [Redshift](../datawarehouse-connectors/redshift-connector.md), [Snowflake](../datawarehouse-connectors/snowflake-connector.md))
- **Create custom event properties** for deeper insights
- **Use AI-powered suggestions** for comprehensive event coverage
- **Export for different platforms** (web, mobile, server-side)

## Common Quick Start Issues

### Figma Import Problems
**Issue**: "Cannot access Figma file"
**Solution**: Ensure you have read access and enable "Viewers can copy, save, and export" in share settings

### Event Import Problems  
**Issue**: "No events found in imported file"
**Solution**: Verify the CSV export includes events and properties, not just raw data

### Missing Event Suggestions
**Issue**: "AI didn't suggest events for my elements"
**Solution**: Try clicking different element types, or manually create events based on user actions

## Success Metrics

You'll know you're on the right track when:
- ✅ **All key user actions** have events assigned
- ✅ **Event names are consistent** and descriptive
- ✅ **Properties provide context** for analysis
- ✅ **Implementation specs are clear** for developers

## Get Help

- **Join our [Slack community](https://join.slack.com/t/glazedanalytics/shared_invite/zt-27kt7tl3n-lkfs1mzqCzyVSKdkiQx2sA)** for quick questions
- **Email [hello@glazedanalytics.com](mailto:hello@glazedanalytics.com)** for technical support
- **Check the detailed guides** in this documentation for specific topics

Ready to dive deeper? Continue with our comprehensive [Getting Started guides](import-figma-files.md) or jump into the [Quick Dev Onboarding](../quick-dev-onboarding/) for implementation details.

**Congratulations! 🎉 You've just created your first visual tracking plan. Welcome to the future of analytics implementation.**