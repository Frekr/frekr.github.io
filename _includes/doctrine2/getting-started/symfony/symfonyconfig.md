####Configuring Database Connections

Configure `config/databases.yml` for database connection:
~~~
all:
  doctrine:
    class: sfDoctrineDatabase
    param:
      options:
        driver: pdo_mysql
        user: root
        password:
        dbname: doctrine
~~~

####Configuring Your Schema

Below is an example of a simple User entity:
~~~
# config/doctrine/schema.yml
 
Models\User:
  type: entity
  table: user
  id:
    id:
      type: integer
      generator:
        strategy: AUTO
  fields:
    username:
      type: string
      length: 255
    password:
      type: string
      length: 255
~~~
