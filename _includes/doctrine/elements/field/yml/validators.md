~~~yaml
  column:
    item:
      notnull: true
      values: [item_archived, item_new, item_available, item_cannot_lend]
      collation: utf8_unicode_ci
      fixed: true
      notblank: true
      country: false
      creditcard: false
      date: false
      email: false
      future: false
      htmlcolor: false
      ip: false
      minlength: 1
      nospace: true
      past: false
      readonly: false
      regexp: item_*
      range: 0,999
      scale: 2
      unsigned: true
      usstate: false
~~~