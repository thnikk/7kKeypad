## Code for 7K+ keypads

This code has changed a bit from what I had originally. I started over with the base code for the trinket M0 and tried using nicohood's library instead of the keyboardio fork which used weird names for all of the keys, which meant that I wasn't able to do a simple char to int conversion for the remapper and instead wuld hve had to search for the value in an array and use a corresponding value in another array to assign the key and the same thing backwards (basically just a huge hastle.) This works a lot better and I'm not sure if I ever had a reason not to use this, but I'm pretty sure it was just because I didn't see that there was NKRO support with the library and thought it was only available in the keyboardio one.

I'm considering adding the LED mode and brightness selection to the remapper like what I have on the touchPad. Since the side button isn't quite as necessary on this one, I may just leave it hardcoded as escape and keep the mode and brightness changing with the button but also have it be available in the remapper, just to make it simpler for people that don't want to mess around with holding the button. I could also just make this functionality configurable, which might make more sense and only thought of right now (when in doubt, leave it up to the user?)

### To do:
- [x] Get NKRO working
- [x] Get LED effects working and stagger cycle mode with the middle (last) key be colored correctly
- [ ] Add EEPROM init (conditionally since this isn't required for the m0 as it uses flash as EEPROM and wipes on upload)
- [ ] Merge this code with the trinket M0 code 
- [ ] Re-add mouse support