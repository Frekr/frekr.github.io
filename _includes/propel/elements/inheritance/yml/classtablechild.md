~~~yaml
  book:
    id:
      type: integer
      required: true
      autoIncrement: true
      primaryKey: true
    cover:
      type: string
    _uniques:
      IX_UQ_book_id: [id]
~~~
