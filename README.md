

the implementation principles briefly in four main points:

Global Game Parameters:

The game involves numerous parameters like the number of slots and layers. To enhance adaptability and customization, we consolidate these parameters into unified global variables. This approach allows for easy modification, automatically adjusting the game accordingly. Additionally, user-friendly pages can be implemented to enable players to customize these parameters, enhancing overall gameplay.
Grid Structure:

To ensure a regular distribution of blocks and simplify coordinate calculations, the game canvas is divided into a virtual 24 x 24 grid, akin to a chessboard. Each block occupies a 3 x 3 grid space, providing a structured layout for efficient gameplay.
Randomly Generated Blocks:

Randomly generating blocks involves determining both patterns and coordinates. Starting with calculating the total number of blocks based on global parameters, the array storing all animal patterns is shuffled. Subsequently, blocks are filled sequentially with these patterns. The coordinate generation principle involves selecting random points within specified coordinate ranges. As the game progresses, the coordinate range may decrease, intensifying the challenge by creating more crowded patterns with each level.
Block Overlay Relationship:

Ensuring a proper order of clicks (upper block before lower block) requires establishing a hierarchical attribute for each block. Two approaches are considered:
First Approach: Generate blocks layer by layer, evaluating the highest-level blocks in each grid to determine if there are blocks in surrounding grids with a higher level.
Second Approach (Chosen): Implement block overlay relationships during random block generation, establishing a hierarchy of block coverage (i.e., determining which block covers another). This method is preferred for its efficiency and streamlined implementation.






