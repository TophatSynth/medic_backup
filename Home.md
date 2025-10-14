
```base
filters:
  or:
    - file.tags.contains("anki")
    - file.tags.contains("tofinish")
properties:
  file.folder:
    displayName: Folder
  file.name:
    displayName: NEEDS WORK DONE
views:
  - type: table
    name: Table
    order:
      - file.name
    sort:
      - property: file.ctime
        direction: DESC
    columnSize:
      file.name: 400

```

```base
filters:
  and:
    - file.ctime > now() - "9 days"
    - not:
        - file.infolder('Attachments')
    - file.name != "Home"
properties:
  file.folder:
    displayName: Folder
  file.name:
    displayName: Lesson
views:
  - type: table
    name: TOC
    order:
      - file.folder
      - file.name
    sort:
      - property: file.folder
        direction: DESC
      - property: file.ctime
        direction: DESC
    columnSize:
      file.folder: 160

```

[[Feedback for MD2001]]
### 4 hours of scheduled activities, 4.5 hours of independent studies per day