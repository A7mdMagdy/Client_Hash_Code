This project consists of two parts:
1) Dispatcher: This part extracts data from work item pages and filters it to select work items with WI5 type only. The filtered data is then loaded into a queue in the orchestrator.
2) Performer: This component navigates to each item in the queue, extracts the client ID, client name, and client country, combines them, and then visits the SHA1 site to obtain the security hash code.
   This hash code is then used to update the item, marking its status as Completed.
