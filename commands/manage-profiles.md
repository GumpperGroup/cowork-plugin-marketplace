---
description: View, add, update, or audit your profile URL tracker. Maintains a list of every platform where your bio appears, with status tracking and update reminders.
allowed-tools: Read, Write, Edit, Glob, WebFetch, WebSearch
---

# Manage Profiles

Manage the centralized profile URL tracker. Uses the `profile-management` skill.

## Actions

Based on `$ARGUMENTS` or user intent, perform one of:

### View Profiles
Display the current profile tracker table. If no tracker exists yet, offer to create one.

### Add Profile
Add a new platform URL to the tracker:
1. Ask for: Platform name, URL, which bio version is published, date last updated
2. Add to the tracker table
3. Set initial status based on bio freshness

### Update Profile
Mark a profile as updated:
1. Ask which platform was updated
2. Record the new date and bio version used
3. Set status to ✅ Current

### Remove Profile
Remove a URL from the tracker (e.g., if the agent leaves a platform).

### Audit All Profiles
Review every URL in the tracker:
1. Check each for accessibility
2. Compare published bios against latest optimized versions
3. Flag inconsistencies and outdated content
4. Update status for each profile
5. Recommend any missing Tier 1 or Tier 2 platforms

### Gap Analysis
Compare the agent's tracked profiles against the recommended platform list and identify:
- Missing Tier 1 platforms (critical)
- Missing Tier 2 platforms (important)
- Platforms with stale or outdated bios
- Opportunities for additional coverage

## File Persistence

Save the tracker to the user's working directory as `profile-tracker.md`. Load it automatically if it exists. Always ask before overwriting.
