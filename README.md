# Hercules P32 DJ Mapping by Sebastian Teister
## Conventions
### Documentation inside Traktor 2
Each Traktor Function is documented at least with the corresponding corntol on the P32 in the *comment* field.
### Syntax and Naming
Buttons are being written in [], like [Play].  
Matrix buttons are being named with their number only, like [16], where the bottom left buttons is [1], then right and up the rows:  
  [13][14][15][16]  
  [ 9 ][10][11][12]  
  [ 5 ][ 6 ][ 7 ][ 8 ]  
  [ 1 ][ 2 ][ 3 ][ 4 ]  
  When there is a modifier where a button is active it's written behind the button in \<>, e.g. [Play]\<Hotcue>, which means the button [Play] is only active when the \<Hotcue> modifier is selected.
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
