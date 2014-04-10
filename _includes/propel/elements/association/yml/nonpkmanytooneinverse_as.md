~~~yaml
  publisher:
    id:
      primaryKey: true
    name:
      type: string
    vatCode:
      type: string
      required: true
    _uniques:
      IX_UQ_publisher_id: [id]
~~~