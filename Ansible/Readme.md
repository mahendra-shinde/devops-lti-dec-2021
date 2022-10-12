## YAML / Yet Another Markup Language

YAML is derived from JSON.


> Simple String values

```json
"name" : "Mahendra"
```

```yaml
name: mahendra
```
 Note : There must be NO SPACE before ":"

> Array or List

```json
"months" : [ "Jan","Feb","Mar" ]
```

```yaml
months:
- Jan
- Feb
- Mar
```

> Object

```json
"person": {
    "firstName" : "Mahendra",
    "lastName"  : "Shinde" 
}
```

```yaml
person: 
  firstName: Mahendra
  lastName: Shinde
```

There is an INDENT before "firstName" and "lastName"
    An ident is either 2 or 4 spaces. (It could be 6 or 8 spaces).
    NEVER USE "TAB" on Windows Notepad. YAML doen't support TABs
    Smart text editors like VSCode may convert the TABs into Spaces.