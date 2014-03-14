~~~yml
  manyToOne:
    publisher:
      targetEntity: publisher
      inversedBy: itemRecord
      joinColumns:
        publisherId:
          referencedColumnName: publisher_id
          nullable: false
~~~
