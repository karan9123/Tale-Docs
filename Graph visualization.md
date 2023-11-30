
### Algorithm Overview

1. **Initialization**:
    
    - Set card sizes for tier 1, tier 2, and tier 3 connections.
    - Set the maximum number of users to be displayed at any time to 50.
2. **Displaying Tier 1 Connections**:
    
    - Place tier 1 connection cards close to the central user card without overlapping.
    - Size of tier 1 connection cards should be slightly smaller than the central card.
    - For each tier 1 connection, check if they have their own tier 1 connections.
        - If a connection has more than 2 tier 1 connections (including the current user), connect it to the central user with a line and display up to 3 of its own tier 1 connections in smaller size.(Basically create a small cluster of user's upto 3 tier 1 connections and connect it using a line)
        - If a connection has 2 or fewer tier 1 connections, display it without a line.
1. **Displaying Tier 2 Connections**:
    
    - Check if the total number of displayed users (including tier 1 and their connections) is less than 50.
    - If yes, display tier 2 connections farther from the central user card, ensuring they form a distinct cluster.
    - Apply the same rules for tier 2 connections as for tier 1 regarding their own tier 1 connections.
4. **Displaying Tier 3 Connections**:
    
    - Similar to tier 2, check if adding tier 3 connections exceeds the limit of 50 users.
    - If not, display them even farther from the central user card, forming another distinct cluster.
    - Follow the same rules for their connections as in tier 1 and tier 2.
5. **Interaction Handling**:
    
    - When a user clicks on a card, display the name and other relevant information.
    - Implement zoom in/out functionality while maintaining the maximum limit of displayed users.



## Pseudocode

```
Algorithm ForceDirectedGraphLayout
    Inputs: userData (array of user nodes and their connections)

    // Step 1: Initialization
    Initialize graphNodes from userData
    Initialize graphLinks between nodes based on user connections
    Define graph parameters (like dimensions, node size, repulsion strength, etc.)

    // Step 2: Setting up Force Simulation
    Define a Force Simulation
    Apply forces to the simulation:
        - Link Force: Define links between nodes based on user connections
        - Charge Force: Define repulsion force among nodes to avoid overlap
        - Center Force: Optionally, define a force to keep nodes centered
        - Collision Force: Define a force to prevent nodes from overlapping

    // Step 3: Running the Simulation
    While simulation is running
        Update node positions based on applied forces
        Update link positions corresponding to their nodes

    // Step 4: Rendering the Graph
    For each node in graphNodes
        Render node at its current position
    For each link in graphLinks
        Render link connecting the corresponding nodes

    // Step 5: Handling User Interaction
    Define interactions such as clicking on a node
    On interaction, perform actions like displaying user details

    // Step 6: Adjustments and Updates
    If userData changes or adjustments are needed
        Update graphNodes and graphLinks
        Restart the force simulation with updated data

    // Step 7: Cleanup and Stopping the Simulation
    On completion or when required
        Stop the force simulation
        Perform necessary cleanup

End Algorithm

```


###  **Data Model Assumption**
    
- The data is stored in a PostgreSQL database with a relationship table having fields: `Id`, `related_from`, `related_to`, `relation_name`, `relation_tier`, `created_date`, `updated_date`.
- Here `relation_name` is from a list of [[Relations]] stored in the backend.

## Algorithm

1. **Initialization**
   
- Sets up the initial data structure, converting user data into a format suitable for a graph layout (nodes and links).
- Set constants like `MAX_USERS`, and define card sizes and other relevant parameters.
- Initialize state and/or refs in React to manage the graph data and SVG elements.

2. **Data Fetching and Preparation**
   
- Fetch user relationship data from the database.
- Format the data to suit the requirements of a force-directed graph (i.e., nodes and links structure).
  
3. **Setting up Force Simulation**
   
- Defines the various forces that will act upon the nodes (user cards) and links (connections).
- These forces determine how the nodes and links interact with each other, ensuring a balanced and readable layout.
-  Create an SVG element within the React component to hold the graph.
- Define a force simulation with forces like `forceLink`, `forceManyBody`, `forceCenter`, and `forceCollide` to control the behavior of nodes and links.
  
4. **Running the Simulation**
   
- The main loop where the position of each node and link is updated based on the forces applied. This step is crucial for achieving the desired layout.
  
5. **Rendering the Graph**
   
- Translates the abstract positions of nodes and links from the simulation to visual elements.
- This step will vary depending on the rendering method used (e.g., SVG, Canvas).
   
6. **Handling User Interaction**
   
- Implement React event handlers for user interactions like clicking on a node to display more information.
   
7. **Adjustments and Updates**
   
- This allows for the dynamic updating of the graph when the underlying data changes or when the user makes adjustments.


## Libraries to check:
- d3.js
- react-force-graph

## Going with:
- Apollo and graphQL 
