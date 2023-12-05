### Minutes of the Meeting on [Nov 17, 23]

**Main Points Discussed:**

1. **Limit on Displayed Users:**

   - It was agreed that at any given time, the maximum number of users displayed on the page should not exceed 50. This limit includes any scaling or zooming adjustments.

2. **Tier 1 Connection Display Rules:**

   - Tier 1 connection cards will be displayed close to the central user card. This proximity will serve as an indicator of their Tier 1 status.
   - The visual representation of Tier 1 connection cards should be slightly smaller than the central user's card.
   - Special Rule for Tier 1 Connections:
     - If a Tier 1 connection has more than 3 users as their own Tier 1 connections (including the current user), this connection will be distinguished with a line.
     - Up to 3 of these additional Tier 1 connections will be shown in smaller size near the primary Tier 1 connection.
     - Tier 1 connections with less than 3 own Tier 1 connections will be displayed without additional lines or connections.

3. **Tier 2 Connection Display Rules:**

   - Tier 2 connections will be displayed only if the total number of Tier 1 users and their connections do not fill the 50-user quota.
   - These connections should be positioned farther from the central card, in a different direction, forming their own cluster.
   - Tier 2 connections will follow the same display rules as Tier 1 for their own connections.

4. **Tier 3 Connections:**
   - Tier 3 connections will be handled similarly, displayed in a way that follows the same principles as Tier 1 and Tier 2.

**Next Steps:**

- Karan will incorporate these guidelines into the user connections visualization algorithm.
- We will meet around Wednesday to discuss further.

**Additional Notes:**

- There was a consensus on the importance of maintaining a clear and intuitive user interface, especially when handling a large number of connections.

---
### Minutes of the Meeting on [Nov 27, 23]

**Agenda:**

1. Review of the previous meeting's decisions on user connection displays.
2. Discussion of new updates and changes to the user connection algorithm.
3. Assigning tasks and setting next steps.

**Discussion and Decisions:**

1. **Modification in Tier 1 Connection Rules:**
    
    - **Update on Relations for Forming Clusters:** The number of relations required for a Tier 1 connection to form their own cluster has been reduced from 3 to 2 (including the current user as a relation).
      
2. **Input Requirements for Identifying Links in Relationships:**
    
    - **Task for Karan:** Determining all the inputs required from users to identify links in their relationships.
    - **Example Scenario:** When a nephew sends a connection request, both the nephew and the user should have the ability to select a common person (e.g., their parent and the user's sibling) as the reason for the connection.
      
3. **Review of Apollo Library with GraphQL:**
    
    - **Task for Karan:** Review the Apollo library in conjunction with GraphQL to ascertain if it can be utilized effectively for our graphical display use case.
      
4. **Development of Interaction Logic:**
    
    - **Interactive Feature Development:** There is a need to develop a logic for handling interactions within the connections display. This includes how users interact with the connection tiers and the information displayed.
      This also includes handling removal and insertion of the connected users.

**Next Steps:**

- Task 3 is on priority and Milton and Karan will meet on [Nov 28] to discuss further.
- Karan to work on the assigned tasks and present the findings and developments in the next meeting.
- A follow-up meeting will be scheduled to review progress and discuss any further adjustments needed based on Karan's findings.
---
### Minutes of the Meeting on [Nov 30, 23]


**Agenda:**

- Review of progress on user connections visualization algorithm.
- Discussion on the creation of a table for paths for all the identified relations in the tiers.

**Discussion and Decisions:**

1. **Progress on User Connection Visualization Algorithm:**
    
    - The modification in Tier 1 connection rules, reducing the number of relations required to form a cluster from 3 to 2, was successfully incorporated.
2. **Creation of a Table for Relationship Paths:**
    
    - It was decided that Karan will complete table outlining paths for all the relations identified across the tiers.
3. **Prototyping the Algorithm:**
    
    - Karan will start prototyping phase for the user connection visualization algorithm.

4. **Next Steps:**
    
    - Karan will continue working on the table for relationship paths and the prototyping of the algorithm.

**Action Items:**

- Karan to complete the table for relationship paths and proceed with the algorithm's prototyping.
- Schedule a follow-up meeting to review progress and discuss next steps.

---
### Minutes of the Meeting on [Dec 05, 23]

Agenda:

- Review of previous meetings' decisions and progress.
- Discussion on the backend development and prioritization of tasks.
- Outlining and planning the next steps for backend API development.

Discussion and Decisions:

1. **Focus on Backend Development**:
    
    - Karan will primarily focus on backend development, following up on the previous meetings' discussions about user connection visualization and relationship path tables.
2. **Prioritizing Action Items**:
    
    - The immediate priority for Karan is to complete the task of outlining paths for all the relations identified. This includes finalizing the table for relationship paths discussed in the previous meeting.
3. **Backend API Development**:
    
    - Once the relationship paths are outlined, Karan will shift his focus to backend API development.
    - The primary focus will be on developing the 'Read' operation out of the four CRUD (Create, Read, Update, Delete) operations. This step is crucial for ensuring efficient data retrieval.
4. **Progression to Other CRUD Operations**:
    
    - After establishing 'Read' operation, Karan will then move on to the development of the remaining CRUD operations - Create, Update, and Delete.
    - This approach will ensure a systematic and efficient development process, prioritizing the most critical operation first.
Next Steps:

- Karan will first complete the outlining of paths for all the identified relations.
- Upon completion, the focus will shift to the development of the backend API, starting with the 'Read' operation.
- Sequential development of the other CRUD operations will follow.

Action Items:

- Karan to finalize the table for relationship paths as a priority.
- Begin the backend API development focusing initially on the 'Read' operation.
- Plan for the sequential development of the remaining CRUD operations.
