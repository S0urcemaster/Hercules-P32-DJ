# Hercules P32 DJ Mapping for Traktor Pro 2
@Author: Sebastian Teister

**Documentation not finished yet!**

## Where Am I?
Hercules P32 DJ is a hardware MIDI DJ controller for the Traktor Pro 2 DJ Software which allows user programming of it's functions through MIDI controllers.

## Conventions

### Documentation in Traktor 2 Controller Editor
Each Traktor Function is documented at least with the corresponding corntol on the P32 in the *comment* field of the Traktor Controller Editor. If you're searching a specific function you can either look for the Traktor function in the "Control" column or the P32 control name in the comment column.

### Syntax and Naming in the Comment Field
Controls are written in brackets [], like [Play].  
Matrix buttons are named with their number only, like [16], where the bottom left buttons is [1], then right and up the rows:  

  [13][14][15][16]  
  [ 9 ][10][11][12]  
  [ 5 ][ 6 ][ 7 ][ 8 ]  
  [ 1 ][ 2 ][ 3 ][ 4 ]  
  
When there is a modifier where a button is active it's written behind the button in \<>, e.g. [Play]\<Hotcue>, which means the function can only be activated when pressing [Play] when \<Hotcue> modifier is selected.

When a shift modifier is needed to activate a function a ^ is written before the control name, e.g. [^16], which means you need to press [Shift] and then [16].

## General Workflow
### Buttons That Work as Modifiers
- **Shift** is an P32 internal modifier and changes the Midi message that is generated
- **LoadA** Traktor Modifier. Switches DeckA and Deck C
- **LoadB** Not used yet
- **Sampler**, **Slicer**, **Loop**, **Hotcue** P32 internal modifiers switching the matrix buttons which generate different Midi messages. Also used in Traktor for extra switching.

**Hotcue**, **Loop**: *Standard* setting where all controls work as usual.  

**Slicer**: *Special* setting where some controls work differently.
- [Fx1] to [Fx3] work as FX knobs.  
- [Fx1 ON] to [Fx3 ON] work as FX buttons.  
- [Dry/Wet] is FX Dry/Wet  
- [Macro] is FX On

#### Modifiers Traktor Internal
- LoadA = Modifier2 toggle 0/1
- LoadB = Modifier3 toggle 0/1
- Sampler/Slicer/Loop/Hotcue **left** side = Modifier4 0/1/2/3
- Sampler/Slicer/Loop/Hotcue **right** side = Modifier5 0/1/2/3
