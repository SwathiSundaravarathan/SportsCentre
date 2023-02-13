Swathi Sundaravarathan LAB 3 ReadmeFile

Creating the demo-Servlet

![image](https://user-images.githubusercontent.com/97709529/152909011-b390342f-cc20-4e67-a6ca-6361d4ef060e.png)

First Run while redirecting

![image](https://user-images.githubusercontent.com/97709529/152909119-fcc5e2de-3aef-4844-b79d-6771c076db2b.png)

Constraint voilations in initial stage

![image](https://user-images.githubusercontent.com/97709529/152909257-89afef8a-8412-4391-9b30-1032c570a2a2.png)

Valid Actor Page

![image](https://user-images.githubusercontent.com/97709529/152909332-c815d948-540d-4d77-8a31-d08ce54533d9.png)

Invalid error messages Page

![image](https://user-images.githubusercontent.com/97709529/152909419-8e5b21fb-5a72-4e2b-b96a-5e9f0a7f61bd.png)

Valid actor Final display

![image](https://user-images.githubusercontent.com/97709529/152909463-74a98022-3e81-4084-9194-5fdfacec7ee5.png)

Inserting into database(valid actor)

![image](https://user-images.githubusercontent.com/97709529/152909568-cc64178e-57d0-4e7b-8075-776f0b0f9710.png)

![image](https://user-images.githubusercontent.com/97709529/152909597-3c0b51e8-17cb-4856-811e-9d82cee73027.png)

Brief summary:

1. Your understanding of the difference between the forward and redirect operations.
Ans: Forward is sending the data directly to other method, redirecting is sending the data and consecutive steps to new function.

2. How would you be validating user submissions without the Bean Validation API
standard?
Ans : By Accessing the database tables and determining the changes.

3. How do you think this approach would scale to a real application with 100's of
entities?
Ans : Time taken for execution may increase as the number if entities increases. Dependencies can be managed.

4. Why didn't we need to include any additional dependencies (i.e. Bean Validation,
JDBC) in this project?
Ans : Because we where servlet, MVC for validation.
