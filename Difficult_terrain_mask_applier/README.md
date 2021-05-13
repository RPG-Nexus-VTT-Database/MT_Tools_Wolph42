# Difficult Terrain Mask Applier

This drop-in copies difficult terrain tokens (or actually any token you would like) in places where a map is non transparent.

The forum source for these files is https://forums.rptools.net/viewtopic.php?f=46&t=28950

The text below is from the forum instructions.

This is a bit more advanced. This drop-in copies difficult terrain tokens (or actually any token you would like) in places where a map is non transparent.
It makes use of the 'Token VBL' option in maptool.

You are probably familiar with 'Token VBL' where the VBL is applied where a token is non transparent. You can use this function for doors, but you can also create a mask of a map in e.g. photoshop. This is what such a mask looks like:
mask image
note here that the white area is actually transparent. The red obviousl not.

If you drag this image on the background layer of MT and then apply token VBL you would get (yellow) VBL in the red areas.

What this macro does is check whether in a cell is token vbl and if so it copy pastes a 'terrain modifier' token (which you have to create yourself) into that spot. The result would look like this:
result image
Explanation:
next to the Hero token you see the original 'terrain modifier' token (small triangle in lower right corner).
- The mask image has been placed onto the background layer (as you can see)
- Token VBL is turned ON for the mask (any existing normal/blue VBL already on the map will be ignored)
- Run the macro on the drop-in
- result is a 'difficult terrain' token in every cell where there is yellow VBL close to the centre of that cell (thats why you don't see any terrain tokens in cells where the mask has bled into).

when done you can remove the mask image.

Usage:
1. drag and drop token into campaign (macro token)
2. place mask on background (mask token)
3. place 'to be copied token, for example a difficult terrain, on the map (terrain token)
4. turn on token VBL for the mask
5. edit first 3 lines of the macro on the 'macro token':
- mTok is the name of the mask token
- dTok is the name of the terrain token
- layer is the layer where you want to have the terrain tokens placed
6. save and run
7. remove mask token.
done.
