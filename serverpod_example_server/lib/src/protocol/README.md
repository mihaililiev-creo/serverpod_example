# Define schemas

Here, we define the schemas we are using in our database. Once defined and after we run `serverpod generate`,
objects will be create which are used to communicate directly with the database.
The `class` property is the name of the generated class; `tables` is the name of the table in the database and `fields` are the columns in the table.
`fields` accepts all `Dart` serializable classes (`bool`, `int`, `double`, `String`, `DateTime`, `ByteData`, ...), which can also be used in `List`s and `Map`s.

## Defining the Todo schema

Starting off by configuring the `todo.yaml` file by the above mentioned standards.

Afterwards we can run `serverpod generate`. This will generate our `Todo` class for communication with our todos table in the database. 
It will also generate a `pgsql` command in the `generated/tables.pgsql` file. To create the todos table, we need to run that command in our database
(either inside the `Docker` container or any postgres manager app such as `Postico` or `pgadmin`). 

Once the table is created, we are free to start working on endpoints and manipulating the todos table data.
