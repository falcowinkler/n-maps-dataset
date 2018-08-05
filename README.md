# n-maps-dataset
Dataset collection of maps for the game n.

The n_maps.tfrecord contains publically available data that has been scraped from http://numa-notdot-net.appspot.com.
Currently there are around 23000 maps available on the website. 
The data has been filtered a bit, it contains around 90000 data items.
Formats are generated with https://github.com/falcowinkler/copicat.

### Format

The .tfrecord file contains a single feature: `raw_tile_data`, which contains the byte encoding for the tiles. 
Tile codes range from 0-33, and each array is 31 * 23 = 713 bytes large. 
As a guideline how to decode it with tensorflow, have a look at https://github.com/falcowinkler/dreamer.
