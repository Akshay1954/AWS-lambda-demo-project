# AWS-lambda-demo-project
A project that automatically deletes EBS snapshots which are not attached to any volumes or when the volumes are deleted by terminating the EC2 instances thus optimizing the cost.


![Screenshot at 2025-03-01 02-00-14](https://github.com/user-attachments/assets/8409045b-706e-4c53-b0af-98a3995e9996)
I have created the EC2 instances.


![Screenshot at 2025-03-01 01-59-31](https://github.com/user-attachments/assets/02493769-ef8e-4bf4-80ce-3cfa144bdd9a)
This is the volume associated to the EC2 instance.

![Screenshot at 2025-03-01 01-58-50](https://github.com/user-attachments/assets/5f6d3b4a-2067-45eb-9f9f-f24027f4ee2d)
Created a Snapshot of the volume.

![Screenshot at 2025-03-01 02-07-22](https://github.com/user-attachments/assets/dbe9bb94-5ece-4843-bb26-2145469d2c3d)
Lambda Function Script in python that detects whether a volume is attached to an running EC2 instance or not and checks if the the snapshot is attached to the volume. If not the it will delete the snapshot. This will help in cost reduction by deleting the unused resources.

![Screenshot at 2025-03-01 01-49-29](https://github.com/user-attachments/assets/bc0efb30-7bd1-487a-8802-5d41100018ae)
IAM roles associated with the function.

![Screenshot at 2025-03-01 02-01-47](https://github.com/user-attachments/assets/b6396535-b6fd-4349-a2fa-8108e3790638)
Demonstrate the working of the lambda function by terminating the EC2 instance by testing manually. You can even make an alarm that runs the script everyday at a specific time.

![Screenshot at 2025-03-01 01-55-28](https://github.com/user-attachments/assets/06a80c6a-f98e-4201-b6c3-663d7b86064b)
Function run successfully

![Screenshot at 2025-03-01 02-05-04](https://github.com/user-attachments/assets/f477f276-d8e9-4038-9ad4-a13b6505b16e)
Snapshot has been deleted successfully.




