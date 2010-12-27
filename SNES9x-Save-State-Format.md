# Header
8 character magic number of "#!snes9x", colon ':' and 4 digit version number followed by new line (ASCII #10). In total, 14 bytes.

# Blocks
Most of the save state data is in blocks. Blocks start with 3 characters for block name, ':', 6 digit payload length, ':' and payload of length specified in bytes. The next block follows immediately, without a separator.  
Example: "`NAM:000144:/Users/Mehdi/Documents/ROMs/Donkey Kong Country 3 - Dixie Kong's Double Trouble/Donkey Kong Country 3 - Dixie Kong's Double Trouble (E) [!].smc