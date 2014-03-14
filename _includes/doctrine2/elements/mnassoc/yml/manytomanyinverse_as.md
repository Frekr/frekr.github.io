~~~yml
author:
  type: entity
  fields:
    id:
  manyToMany:
    itemRecords:
      targetEntity: itemRecord
      mappedBy: authors
~~~
