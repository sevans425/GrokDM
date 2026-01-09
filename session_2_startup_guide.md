     1	# Session 2 Startup Guide
     2	
     3	## For the DM Agent
     4	
     5	When the user says they're ready for session 2, follow these steps:
     6	
     7	### 1. Verify/Get Campaign Data
     8	```
     9	Read: /memories/campaign_data.md
    10	If spreadsheet ID exists: continue
    11	If no spreadsheet ID: Ask user "What is your campaign spreadsheet ID?"
    12	Update campaign_data.md with the user's spreadsheet ID
    13	```
    14	
    15	### 2. Load Session 1 State
    16	```
    17	Read: /memories/session_checkpoints/session_1_complete.md (quick reference)
    18	Read: /memories/session_checkpoints/session_1_summary.md (full details)
    19	```
    20	
    21	### 3. Fetch Current Game State
    22	```
    23	Call: game_state_manager worker
    24	Task: "Load all data from Google Sheet 139NjvmH7wJa2FIlEbCrvxEqMitHSsWmYPMGXXvUmiy8 for session 2 start"
    25	```
    26	
    27	### 4. Provide Recap to Player
    28	Summarize:
    29	- Where Eden is (The Sleeping Bear Tavern, celebrating as hero)
    30	- What was accomplished (portal closed, victims rescued)
    31	- What mysteries remain (unknown idol creator, broader crisis)
    32	- What leads are available (Miriam the Crow-Keeper, investigate Crown of Unity)
    33	
    34	### 5. Set the Scene
    35	Begin session 2 with:
    36	- Time context (next morning? same evening?)
    37	- Eden's immediate situation
    38	- Prompt for player action
    39	
    40	## Key Information Quick Reference
    41	
    42	**Eden's Status (End of Session 1):**
    43	- HP: 7/7
    44	- Spell Slots: 1st level 2/2 (fully rested)
    45	- Location: The Sleeping Bear Tavern, Thornhaven
    46	- Status: Hero of Thornhaven, has Mayor's authority (seal ring)
    47	
    48	**Immediate Situation:**
    49	- Thornhaven is safe (portal closed)
    50	- But the idol creator is still out there
    51	- Crown of Unity crisis may be kingdom-wide
    52	- Potential leads: Miriam the Crow-Keeper, broader investigation
    53	
    54	**Important NPCs:**
    55	- Mayor Aldric Blackwood (deeply grateful)
    56	- Torvald Copperkettle (eternal gratitude, saved Eden's life)
    57	- Captain Rorick (respect earned)
    58	- Benna Cartwright (generous ally)
    59	- Miriam the Crow-Keeper (not yet met, potential info source)
    60	
    61	**Active Mystery:**
    62	Someone used stolen grimoires to create the portal. Who? Where? Why?
    63	
    64	## Context Management Note
    65	This startup process should require only:
    66	- ~200 tokens to read checkpoint files
    67	- ~1000 tokens to load Google Sheet
    68	- ~500 tokens for recap and scene-setting
    69	
    70	Total: ~1700 tokens to start session 2, compared to potentially 50,000+ tokens if loading full conversation history from session 1.
    71	
    72	This is why the checkpoint system exists!