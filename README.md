# Host Database on Cloud Using Clever Cloud

## Aim

To demonstrate how to host a database on the cloud using **Clever Cloud**.

## Clever Cloud

Clever Cloud is a Platform as a Service (PaaS) designed to help businesses deploy web services in the cloud quickly and efficiently. It offers a pay-as-you-go pricing model, eliminating the need for infrastructure management, system updates, and troubleshooting.

## Algorithm

1. **Create a New Application**: Start by creating a new application on Clever Cloud.
2. **Deploy Your Application**: Deploy your application to the cloud platform.
3. **Check Deployment**: Verify that your application has been successfully deployed.
4. **Configure Your Application**: Set up your application’s configuration settings.
5. **Connect to a Database**: Establish a connection to a database hosted on Clever Cloud.

## Implementation

The following Python code demonstrates how to connect to a MySQL database, perform basic database operations, and interact with the database using `mysql-connector-python`.

```python
  import mysql.connector
  mydb=mysql.connector.connect(
        host=#host,
        database=#database,
        user=#user,
        password=#password)

  mycursor= mydb.cursor()
  mycursor.execute("CREATE TABLE test2(name VARCHAR(255),age int)")
  sql ="INSERT INTO test2 (name,age) VALUES (%s,%s)"
  val=("test1","1")

  mycursor.execute(sql,val)
  mybd.commit()
  sql="UPDATE test2 SET name = 'test4' WHERE name = 'test1'"
  mycursor.execute(sql)
  mydb.commit()
  mycursor.execute("SELECT *FROM test2")
  myresult= mycursor.fetchall()

  for x in myresult:
          print(x)

  sql="DELETE FROM test2 WHERE name='test4'"
  mycursor.execute(sql)
  mycursor.commit()

```

## Output

The output will consist of the results from the `SELECT` query, which displays the contents of the `test2` table after performing various operations like inserting, updating, and deleting records.

![image](https://github.com/user-attachments/assets/39775f72-289c-4d85-bd30-0fe1bdd14a04)


## Result

The implementation of hosting a database on Clever Cloud was successfully created and executed, demonstrating how to manage a cloud-hosted database using basic SQL operations.

