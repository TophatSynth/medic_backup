### 4 hours of scheduled activities, 4.5 hours of independent studies per day

```base
filters:
  and:
    - file.ctime > now() - "2 weeks"
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
    name: Table
    order:
      - file.folder
      - file.name
    sort:
      - property: file.folder
        direction: DESC
      - property: file.ctime
        direction: DESC
    columnSize:
      file.folder: 200

```

[[Feedback for MD2001]]