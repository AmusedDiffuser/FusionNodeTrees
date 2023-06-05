# DaVinci Resolve Fusion FG_BG_decompose_wMask Node Setup

## Description

This project contains a .settings file that can be dragged into DaVinci Resolve Fusion to create a node tree that performs the following tasks:

- Make a selection with the magic mask tool on a source footage
- Export an image sequence of the masked area to a specified folder
- Export an image sequence of the unmasked area to a separate folder
- Load back the processed image sequences into the original masked area and background
- Output another image sequence of a black and white representation of only the mask

## Installation

To install the .settings file, you need to drag and drop it into DaVinci Resolve Fusion. This will create the node tree automatically.

## Usage

To use this node setup, you need to adjust some settings according to your needs. Here are some steps to follow:

- In the MediaIn1 node, browse and select your source footage that you want to mask
- In the MagicMask1 node, choose between Person Mask or Object Mask, and use the brush tool to refine your selection
- In the Saver1 node, browse and choose a location and a name for your masked image sequence
- In the Saver2 node, browse and choose a different location and a name for your unmasked image sequence
- In the MediaIn3 node, browse and select the processed masked image sequence from the same folder as in Saver1 node
- In the MediaIn4 node, browse and select the processed unmasked image sequence from the same folder as in Saver2 node
- In the Merge3 and Merge4 nodes, adjust the BackgroundAlpha parameter to control how much of the background image is visible in the final result
- In the Saver3 node, browse and choose a location and a name for your mask image sequence

To render your image sequences, go to the Fusion menu and select Render All Savers. This will save your image sequences to the chosen folders.

You can also view the output of each Merge node by connecting it to a MediaOut node.
