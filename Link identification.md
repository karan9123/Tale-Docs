## User interface components

- Dropdown lists or search fields to select the type of [[Relationships]] (e.g., parent, sibling, cousin).
- An option to specify the common person linking the two users.
- Ability to add new relationship types or roles if not listed.

1. **Initial Relationship Selection**:
    
    - The user selects the primary relationship from the first dropdown (e.g., 'Grandfather').
2. **Triggering Secondary Dropdown**:
    
    - Based on the selection, a secondary dropdown is triggered. For instance, if 'Grandfather' is chosen, the second dropdown asks which parent this grandfather is related to.
3. **Dynamic Secondary Dropdown**:
    
    - The secondary dropdown should dynamically populate with relevant options. For example, if the user has already added their parents to the app, these names should appear in the dropdown.
4. **Handling Non-User Parents**:
    
    - If the parent is not a user or hasn't been added yet, provide an option like "Add New Parent." This allows the user to input the name of the parent, creating a placeholder in the relationship map.
5. **Placeholder Integration**:
    
    - When a new parent name is entered, the system creates a non-user entity in the database. This entity acts as a placeholder and can be linked to other family members.
6. **Updating Relationships**:
    
    - Provide options for users to update these relationships, especially if the placeholder parent later becomes a user or if there are changes in the family structure.