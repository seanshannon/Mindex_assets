# Terminator Text Effect for Unity

This package provides scripts to create the iconic "MYNDEX" text with Terminator-style effects, including the camera zoom-out animation and the signature glint effect that sweeps across the text.

## Features

- **Terminator-style font rendering** with alien green color
- **Camera zoom-out animation** that starts close and pulls back to reveal the full text
- **Glint effect** that sweeps from left to right across the text
- **Custom shader** for authentic visual effects
- **Easy setup** with automatic scene configuration

## Setup Instructions

### Method 1: Automatic Setup (Recommended)

1. Create an empty GameObject in your scene
2. Add the `TerminatorTextSetup` component to it
3. The script will automatically:
   - Create a Canvas if none exists
   - Set up the main camera
   - Add the TerminatorTextEnhanced component
   - Configure all necessary components

### Method 2: Manual Setup

1. **Create Canvas** (if not exists):
   - Create empty GameObject
   - Add Canvas component
   - Set Render Mode to "Screen Space - Overlay"
   - Add CanvasScaler and GraphicRaycaster components

2. **Set up Camera**:
   - Ensure you have a Main Camera
   - Set background color to black
   - Set Clear Flags to "Solid Color"

3. **Add Terminator Text**:
   - Create empty GameObject
   - Add `TerminatorTextEnhanced` component
   - Assign the Canvas and Camera references
   - Set the desired font (Terminator-style recommended)

## Font Requirements

For the most authentic look, you'll need a Terminator-style font. You can:

1. **Use a Terminator font**: Download a Terminator-style font and place it in `Resources/Fonts/Terminator.ttf`
2. **Use default font**: The script will fall back to Arial if no Terminator font is found
3. **Create custom font**: Import your own Terminator-style font and assign it in the inspector

## Customization Options

### Text Settings
- `text`: The text to display (default: "MYNDEX")
- `fontSize`: Size of the text (default: 120)
- `textColor`: Color of the text (default: Alien green)
- `glintColor`: Color of the glint effect (default: White)

### Animation Settings
- `zoomDuration`: How long the camera zoom takes (default: 4 seconds)
- `glintSpeed`: Speed of the glint effect (default: 1.5)
- `glintWidth`: Width of the glint effect (default: 0.15)
- `glintIntensity`: Intensity of the glint (default: 2.0)
- `glintDelay`: Delay before glint starts (default: 0.8 seconds)

## Scripts Included

### TerminatorTextEnhanced.cs
The main script that handles:
- Text creation and positioning
- Camera zoom animation
- Glint effect with custom shader
- Material management

### TerminatorTextSetup.cs
Helper script for easy scene setup:
- Automatic Canvas creation
- Camera configuration
- Font loading
- Component assignment

### TerminatorText.cs
Simpler version with basic glint effect (fallback option)

## Usage Example

```csharp
// The script will automatically start when the scene loads
// You can also trigger it manually:

TerminatorTextEnhanced terminatorText = GetComponent<TerminatorTextEnhanced>();
if (terminatorText != null)
{
    // Customize settings
    terminatorText.text = "CUSTOM TEXT";
    terminatorText.fontSize = 150;
    terminatorText.textColor = Color.cyan;
}
```

## Troubleshooting

1. **Text not visible**: Check that Canvas is set up correctly and Camera is assigned
2. **No glint effect**: Ensure the custom shader is working (fallback to basic version available)
3. **Font issues**: Make sure font is assigned or available in Resources folder
4. **Performance**: Adjust glint speed and intensity if needed

## Notes

- The effect works best with dark backgrounds
- For best results, use a Terminator-style font
- The glint effect uses a custom shader for authentic appearance
- Camera zoom starts very close and pulls back to reveal the full text
- All animations are smooth and use easing functions for natural movement

## Credits

Inspired by the iconic opening credits of "The Terminator" (1984) directed by James Cameron. 
