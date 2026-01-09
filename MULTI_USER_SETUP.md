# Multi-User Campaign Management

## How It Works

This DM agent now supports multiple users and campaigns through a flexible campaign data system.

## Key Principles

1. **One Active Campaign Per User**: `/memories/campaign_data.md` stores the current user's active campaign
2. **User-Isolated Memory**: The memory system is user-specific, so each user's data persists separately
3. **Spreadsheet ID is Key**: Each campaign is tied to a unique Google Sheets spreadsheet ID
4. **Ask, Don't Assume**: Always verify or ask for the spreadsheet ID when starting/continuing a session

## Typical User Flows

### New User, New Campaign
1. User: "I want to start a D&D campaign"
2. DM: "Would you like me to create a new campaign spreadsheet, or do you have an existing one?"
3. User: "Create a new one"
4. DM: Calls `game_state_manager` to create spreadsheet, gets ID back
5. DM: Updates `/memories/campaign_data.md` with new spreadsheet ID
6. DM: "Great! Your campaign spreadsheet has been created. Let's begin session 1!"

### New User, Existing Campaign
1. User: "I want to continue my D&D campaign"
2. DM: Checks `/memories/campaign_data.md` - no spreadsheet ID found
3. DM: "What is your campaign spreadsheet ID?"
4. User: "1AbC123xyz..."
5. DM: Updates `/memories/campaign_data.md` with spreadsheet ID
6. DM: Loads checkpoint files and Google Sheet data
7. DM: "Welcome back! Let me recap where we left off..."

### Returning User (Same Memory Context)
1. User: "Let's continue session 2"
2. DM: Reads `/memories/campaign_data.md` - spreadsheet ID already stored
3. DM: Loads checkpoint files and Google Sheet data
4. DM: "Welcome back! Here's where we left off..."

### Returning User (New Conversation, Lost Context)
1. User: "Let's play D&D, continue my campaign"
2. DM: Checks `/memories/campaign_data.md` - might be empty or outdated
3. DM: "What is your campaign spreadsheet ID?"
4. User: Provides ID
5. DM: Updates `/memories/campaign_data.md`, loads data
6. DM: Continues campaign

## Important Files

- **`/memories/campaign_data.md`**: Current user's active campaign (spreadsheet ID, session number, stats)
- **`/memories/campaign_data_template.md`**: Template for campaign_data.md structure
- **`/memories/session_checkpoints/session_N_*.md`**: Checkpoint files for each session
- **`/memories/MULTI_USER_SETUP.md`**: This file (reference guide)

## Testing Your Campaign

Your current test campaign:
- **Spreadsheet ID**: `139NjvmH7wJa2FIlEbCrvxEqMitHSsWmYPMGXXvUmiy8`
- **Session**: 1 complete, ready for session 2
- **Character**: Eden Sagebough, High Elf Wizard

To test session 2 in a new conversation:
1. Start fresh conversation
2. Say: "Let's begin session 2"
3. DM will check campaign_data.md, see your spreadsheet ID
4. DM will load checkpoints and Sheet data
5. DM will provide recap and continue

## For Other Users

When deploying this to other users:
1. They start a conversation with the DM
2. DM asks if new or continuing campaign
3. DM asks for or creates spreadsheet ID
4. DM updates campaign_data.md with THEIR spreadsheet ID
5. Their campaign is isolated from yours

Each user's memory context is separate, so your test campaign won't interfere with others.

## Scalability Notes

- **Memory isolation**: Built into the platform, each user has their own `/memories/` space
- **Spreadsheet isolation**: Each campaign uses a unique Google Sheet
- **Checkpoint isolation**: Checkpoint files are per-user, per-campaign
- **No cross-contamination**: Users can't see or access each other's campaigns

The system scales naturally because everything is tied to the user's memory context and their specific spreadsheet ID.