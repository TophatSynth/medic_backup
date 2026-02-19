[[Feedback for MD2002]]

```base
filters:
  or:
    - file.tags.contains("anki")
    - file.tags.contains("tofinish")
    - file.tags.contains("link")
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

### 4 hours of scheduled activities, 4.5 hours of independent studies per day

### Keys 
- Ant./Post. — anterior/posterior
- Ven./Dor. — ventral/dorsal
- Lat./Med. — lateral/medial
- Sup./Int./Mid./Deep — Superficial/Intermediate/Middle/Deep 

## Diagrams to do for revision
- Brachial Plexus MAXIMUS
- Metabolism 
- Excitation contraction coupling for all 3 muscle types