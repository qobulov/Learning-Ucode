| Table                      | Relation                 |
| -------------------------- | ------------------------ |
| projects → task_status     | many-to-one              |
| projects → users           | created_by → many-to-one |
| tasks → projects           | many-to-one              |
| tasks → users              | assigned_to & created_by |
| tasks → task_status        | many-to-one              |
| tasks → task_priority      | many-to-one              |
| task_comments → tasks      | many-to-one              |
| task_comments → users      | many-to-one              |
| project_members → projects | many-to-one              |
| project_members → users    | many-to-one              |


[DB Diagram Link](https://dbdiagram.io/d/task-management-6916bdf06735e11170c60603)