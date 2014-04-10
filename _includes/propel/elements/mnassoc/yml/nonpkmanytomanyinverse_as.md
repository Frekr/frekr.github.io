~~~yaml
  author:
    id:
      primaryKey: true
    firstName:
      type: string
    lastName:
      type: string
    _uniques:
      IX_UQ_author_id: [id]
~~~