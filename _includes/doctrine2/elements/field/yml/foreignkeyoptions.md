~~~yml
  manyToOne:
    publisher:
      targetEntity: publisher
      inversedBy: itemRecord
      fetch: EXTRA_LAZY
      orphanRemoval: true
      cascade: ["all", "merge", "persist", "refresh", "remove"]
      joinColumns:
        publisherId:
          referencedColumnName: publisher_id
          nullable: false
          columnDefinition: itemRecord_publisherId
          onDelete: CASCADE
          onUpdate: RESTRICT
~~~ 
