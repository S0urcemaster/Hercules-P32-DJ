# Hercules P32 DJ Mapping for Traktor Pro 2
@Author: Sebastian Teister

**Documentation not finished yet!**
When the documentation is missing something, the specific function is always documented in the Traktor mapping file.

**Mapping not finished yet and might change!** Deck A/B with Hotcues, Loops and the Common-section is considerably outlined, though. That means, a single controller will work for mixing with hotcues and loops.

## Where Am I?
Hercules P32 DJ is a hardware MIDI DJ controller for the Traktor Pro 2 DJ Software which allows user programming of it's functions through MIDI controllers.

## Files

There are several mapping files for the whole thing:

- P32 Common AB (Functions that are mapped with other than the matrix buttons)
- P32 Common CD (Functions that are mapped with other than the matrix buttons)
- P32 Hotcue AB (Function that are mapped with the Hotcue-buttons)
- P32 Hotcue C (Function that are mapped with the Hotcue-buttons)
- P32 Loop AB (Function that are mapped with the Loop-buttons)
- P32 Loop C (Function that are mapped with the Loop-buttons)
- P32 Remix D (Functions for the Remix deck)
- P32 Sampler AB (Function that are mapped with the Sampler-buttons)
- P32 Sampler CD (Function that are mapped with the Sampler-buttons)
- P32 Slicer A (Function that are mapped with the Slicer-buttons)
- P32 Slicer B (Function that are mapped with the Slicer-buttons)
- P32 Slicer C (Function that are mapped with the Slicer-buttons)

*If you have a setup with just 1 P32 device, you only need the AB-files. Browse function are on Sampler CD, though.*

- Hotcue deals with functions for Hotcues
- Loop deals with functions for Looping
- Slicer A/B deals with Stem-functions (not finished yet)
- Slicer C deals with Effects-preferences
- Sampler AB is empty atm
- Sampler CD is empty for C and on D are the browsing functions
- Remix D pools the Hotcue, Loop and Slicer tabs together in one file and deals with Remix functions.
- Slicer D does not exist yet and is planned for the Sequencer-functions.

## Conventions

My mappings might differ from usual DJ controllers. Usually, functions which are important and often used are on top of the access level, without shifting. Functions which are less often used are mapped behind a shift. For example 'delete hotcue' is behind 2 shifts.

### Documentation in Traktor 2 Controller Editor
Each Traktor Function is documented at least with the corresponding control on the P32 in the *comment* field of the Traktor Controller Editor. If you're searching a specific function you can either look for the Traktor function in the "Control" column or the P32 control name in the comment column.

### Syntax and Naming in the Controller Editor's Comment Field
Controls are written in brackets [], like [Play].  
Matrix buttons are named with their number only, like [16], where the bottom left buttons is [1], then right and up the rows:  

  [13][14][15][16]  
  [ 9 ][10][11][12]  
  [ 5 ][ 6 ][ 7 ][ 8 ]  
  [ 1 ][ 2 ][ 3 ][ 4 ]  
  
When there is a modifier where a button is active it's written behind the button in \<>, e.g. [Play]\<Hotcue>, which means the function can only be activated when pressing [Play] when \<Hotcue> modifier is selected.

When a shift modifier is needed to activate a function a ^ is written before the control name, e.g. [^16], which means you need to press [Shift] and then [16].

After the control [name] and an optional \<condition> there might be additional information to help identifying the mapping, like 

## General Workflow

### Short Explanation of the P32 DJ

As a DJ controller, the P32 DJ has no Jog-Wheels. Instead it has button-matrices which additionally are overlayed with the tabs **[Hotcue]**, **[Loop]**, **[Slicer]** and **[Sampler]** and with the **[Shift]**-button. Like that you can have 128 functions per button matrix.

The caption of the tab-buttons correspond to the bundled DJ software and are not necessarily meaningful for Traktor. Thus, only **[Hotcue]** and **[Loop]** reflect the mapped functions. **[Slicer]** and **[Sampler]** do not name their mapped functions.

To access Traktor's hotcue functions, you need to press **[Hotcue]** first and so on.

I know, it's not easy to get into some other person's concept as it's hard to explain alike.

### Buttons That Work as Modifiers
- **[Shift]** is an P32 internal modifier and changes the Midi message that is generated per control.
- **[Sampler]**, **[Slicer]**, **[Loop]**, **[Hotcue]** P32 internal modifiers switching the matrix buttons which generate different Midi messages.
- **[Shift]** + **[Cue]** Only use of that combo is for deleting Hotcues

### Controls That Are Used Regularly (same on AB and CD)

**[Vol-]** and **[Vol+]** are internally wired for headphone volume and are not used for anything else.

- **[Low-]**, **[Mid]**-, **[High-EQ]**
- **[Volume]** Faders
- "Monitor Cue On" (**[Headphone]**)
- **[Sync]**/Master
- **[Cue]**
- **[PLay]**

### Controls for Deck AB not Mapped with the Button Matrix

- **[Size]**/Adjust Jog Turn (yes, sometimes you need it)
- **[^Size]** Tempo Adjust
- **[Filter]**/Move Move with Size of 8
- **[^Filter]** Key Adjust
- **[Browse]** unused
- **[Rec]** unused for AB
- **[Slip]** Modifier to Auto-Tempo-Adjust on Play (changing)
- **[XFader]** unused

#### Effects Section

Different from the control's captions the order here is symmetric for Deck A and B!

Knobs:
- **[Fx1 Amount]**/**[Dry/Wet]** Waveform Zoom Adjust
- **[Fx2]**/**[Fx3]** unused
- **[Fx3]**/**[Fx2]** Gain
- **[^Fx3]**/**[Fx2]** Auto-Gain
- **[Dry/Wet]**/**[Fx1]** Filter

Buttons:
- **[Fx1 On]**/**[Macro]** Waveform Zoom Adjust Reset
- **[Fx2 On]**/**[Fx3 On]** Keylock On/Off
- **[Fx3 On]**/**[Fx2 On]** Flux On/Off
- **[Macro]**/**[Fx1 On]** Loop On/Off

### **[Hotcue]** Tab Deck A/B/C

Decks A/B/C are exclusively used as Track Decks. Deck A and B are planned for use with Stems (should work already but still needs some work).

Changes of Move/Loop Size will be shown in the **[Display]**.

Direct/ no **[Shift]**:

| 1/5/9/13 | 2/6/10/14 | 3/7/11/15 | 4/8/12/16 |
| :---: | :---: | :---: | :---: |
| **[Move Size Dec]** | **[Move Size Inc]** | **[Move +1]** | **[Move +2]** |
| **[Move +4]** | **[Move +8]** | **[Move +16]** | **[Move +32]** |
| **[Hotcue 5]** | **[Hotcue 6]** | **Hotcue 7[]** | **[Hotcue 8]** |
| **[Hotcue 1]** | **[Hotcue 2]** | **[Hotcue 3]** | **[Hotcue 4]** |

With **[Shift]** (Shift+Hotcue will additionally move to the left of the hotcue point at the value of the set move size.):

| 1/5/9/13 | 2/6/10/14 | 3/7/11/15 | 4/8/12/16 |
| :---: | :---: | :---: | :---: |
| **[]** | **[]** | **[Move -1]** | **[Move -2]** |
| **[Move -4]** | **[Move -8]** | **[Move -16]** | **[Move -32]** |
| **[Hotcue 5 + Move Left]** | **[Hotcue 6 + Move Left]** | **[Hotcue 7 + Move Left]** | **[Hotcue 8 + Move Left]** |
| **[Hotcue 1 + Move Left]** | **[Hotcue 2 + Move Left]** | **[Hotcue 3 + Move Left]** | **[Hotcue 4 + Move Left]** |

With **[Shift]** + **[Cue]** (Delete Hotcues):

| 1/5/9/13 | 2/6/10/14 | 3/7/11/15 | 4/8/12/16 |
| :---: | :---: | :---: | :---: |
| **[]** | **[]** | **[]** | **[]** |
| **[]** | **[]** | **[]** | **[]** |
| **[Delete Hotcue 5]** | **[Delete Hotcue 6]** | **[Delete Hotcue 7]** | **[Delete Hotcue 8]** |
| **[Delete Hotcue 1]** | **[Delete Hotcue 2]** | **[Delete Hotcue 3]** | **[Delete Hotcue 4]** |

### **[Loop]** Tab Deck A/B/C

Direct/ no **[Shift]**:

| 1/5/9/13 | 2/6/10/14 | 3/7/11/15 | 4/8/12/16 |
| :---: | :---: | :---: | :---: |
| **[Loop Size Dec]** | **[Loop Size Inc]** | **[Loop Set 1]** | **[Loop Set 2]** |
| **[Loop Set 4]** | **[Loop Set 8]** | **[Loop Set 16]** | **[Loop Set 32]** |
| **[Loop In]** | **[Loop Out]** | **[Loop-]** | **[Loop+]** |
| **[Loop In-]** | **[Loop In+]** | **[Loop Out-]** | **[Loop Out+]** |

With **[Shift]**:

| 1/5/9/13 | 2/6/10/14 | 3/7/11/15 | 4/8/12/16 |
| :---: | :---: | :---: | :---: |
| **[]** | **[]** | **[Backward Loop Set 1]** | **[Backward Loop Set 2]** |
| **[Backward Loop Set 4]** | **[Backward Loop Set 8]** | **[Backward Loop Set 16]** | **[Backward Loop Set 32]** |
| **[]** | **[]** | **[]** | **[]** |
| **[]** | **[]** | **[]** | **[]** |


(Template):

| 1/5/9/13 | 2/6/10/14 | 3/7/11/15 | 4/8/12/16 |
| :---: | :---: | :---: | :---: |
| **[]** | **[]** | **[]** | **[]** |
| **[]** | **[]** | **[]** | **[]** |
| **[]** | **[]** | **[]** | **[]** |
| **[]** | **[]** | **[]** | **[]** |
