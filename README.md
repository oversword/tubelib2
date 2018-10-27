# Tube Library 2 [tubelib2]

THIS MOD IS WORK IN PROGRESS !!!

A library for mods which need connecting tubes / pipes / cables or similar.

This mod is not useful for its own. It does not even have any nodes.
It only comes with a few test nodes to play around with the tubing algorithm.

Browse on: ![GitHub](https://github.com/joe7575/tubelib2)

Download: ![GitHub](https://github.com/joe7575/tubelib2/archive/master.zip)


## Description

Tubelib2 distinguished two kinds of nodes:
- primary nodes are tube like nodes (pipes, cables, ...)
- secondary nodes are all kind of nodes, which can be connected by means of primary nodes

Tubelib2 specific 6D directions (1 = North, 2 = East, 3 = South, 4 = West, 5 = Down, 6 = Up)

All 6D dirs are the view from the node to the outer side
Tubes are based on two node types, "angled" and "straight" tubes.
  
  
         +-------+
        /       /|               +-------+
       +-------+ |              /       /|
       |       | |             /       / |
       |       | |            +-------+  |
       |       | |            |       |  |
       |       | |            |       |/ |
       |       | +            +-------+| +
       |       |/               |      |/
       +-------+                +------+
  
  
All other nodes are build by means of axis/rotation variants based on param2
 (paramtype2 == "facedir").

The 3 free MSB bits of param2 of tube nodes are used to store the number of connections (0..2).

The data of the peer head tube are stored as meta data: "peer_pos" and "peer_dir"

Tubelib2 provides no update mechanism for connected "secondary" nodes.
That means, all secondary nodes have to check their surrounding for any changes, 
based on player interaction and/or on LBM basis.



## Dependencies
default  

# License
Copyright (C) 2017-2018 Joachim Stolberg  
Code: Licensed under the GNU LGPL version 2.1 or later. See LICENSE.txt and http://www.gnu.org/licenses/lgpl-2.1.txt  
Textures: CC0

## Dependencies
default  

## History
- 2018-10-20  v0.1  * Tested against hyperloop elevator.
- 2018-10-27  v0.2  * Tested against and enhanced for the hyperloop mod.

