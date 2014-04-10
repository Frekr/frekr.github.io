~~~yaml
  itemRecord:
    id:
      primaryKey: true
    publisher_name:
      type: string
    publisher_vat_code:
      type: string
    _uniques:
      IX_UQ_itemRecord_id: [id]
    _foreignKeys:
      :
        foreignTable: publisher
        references:
          - 
            local: publisher_name
            foreign: name
          - 
            local: publisher_vat_code
            foreign: vatCode
~~~