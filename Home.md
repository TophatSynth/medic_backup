Guided studies 
- Porfolio 
	- [ ] Drug formulary
	- [x] Personal development plan
	- [ ] CVS examination
	- [x] Infection prevention and ncontrol 
- Histology
	- [ ] Histology of cardiac muscle
	- [ ] Histology of vasculature
	- [ ] Histopathology of myocardial infarction
	- [ ] Blood cultures
- ECG
	- [x] Interactive 12 lead ECG
	- [x] Interactive ECG 2
	- [ ] ECG assessment
- Anatomy
	- [x] Changes to the circulation at birth 
	- [x] Cross sectional anatomy of the thorax
	- [x] Sepsis
	- [ ] Shock
- Other
	- [x] Central lines
	- [x] Errors in patient safety 2
	- [ ] Formative MCQ's

```base
filters:
  and:
    - '!file.folder.contains("MD2001")'
    - or:
        - file.tags.contains("anki")
        - file.tags.contains("link")
        - file.tags.contains("tofinish")
        - file.tags.contains("ask")
    - '!file.folder.contains("MD2002")'
    - file.folder != "Attachments"
    - file.folder != "Other Notes"
    - '!file.tags.contains("tostart")'
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
      - file.tags
    sort:
      - property: file.tags
        direction: DESC
      - property: file.ctime
        direction: DESC

```

```base
filters:
  and:
    - '!file.folder.contains("MD2001")'
    - file.folder != "Attachments"
    - file.folder != "Other Notes"
    - file.tags.contains("tostart")
properties:
  file.folder:
    displayName: Folder
  file.name:
    displayName: CATCHUP
views:
  - type: table
    name: Table
    order:
      - file.name
      - file.tags
    sort:
      - property: file.tags
        direction: DESC
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
- [x] Brachial Plexus MAXIMUS
- [x] Metabolism 
- [x] Excitation contraction coupling for all 3 muscle types
	- Differences of the 3 muscle types
- SNS and PSNS
- Coagulation/clotting/thrombosis pathway