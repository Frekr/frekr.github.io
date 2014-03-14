~~~yml
itemRecord:
  type: entity
  fields:
    name:
      type: string
      unique: true
      length: 255
      nullable: false
      column: itemRecord_name
      columnDefinition: itemRecord_name
      precision: 1
      scale: 1
      version: false
      generator: 
      sequence-generator: 
      options:
        comment: this is field
        unsigned: true
        version: 3
~~~
