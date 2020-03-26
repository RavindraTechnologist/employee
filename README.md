# Employee Project CRUD operations

1. Get all employees Operation Curl Command: 

curl --location --request GET 'localhost:8081/employees'

2. Get employee by Employee Id Operation Curl Command:

curl --location --request GET 'localhost:8081/employee?EmpId=1'

3. Get employee by Email Operation Curl Command:

curl --location --request GET 'localhost:8081/EmployeesByEmail?Email=ravindra.yadav@gmail.com'

4. Create Operation Curl Command:

curl --location --request POST 'localhost:8081/employee' \
--header 'Content-Type: application/json' \
--data-raw '{
     "Name":"Ravindra",
      "Email": "ravindra.yadav@gmail.com",
      "designation": "Associate L2"
    }'
    
5. Update Operation Curl Command:

curl --location --request PATCH 'localhost:8081/updateEmployee/1' \
--header 'Content-Type: application/json' \
--data-raw '{
	"designation":"Senior Associate L2",
	"Email":"abhishek.yadav@gmail.com"
}'

6. Delete Operation Curl Command:

curl --location --request DELETE 'localhost:8081/deleteEmployee/2'
