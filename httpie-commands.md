
# HTTPie Commands – PotterAPI

## Environment Variables
```bash
export BASE_URL=https://potterapi-fedeperin.vercel.app
export LANG=en
export RESOURCE=characters
export INDEX=1
export SEARCH=Weasley
export MAX=5
export PAGE=2
```

## Commands

**1. List Resource**
```bash
http GET $BASE_URL/$LANG/$RESOURCE
```

**2. Get by Index**
```bash
http GET $BASE_URL/$LANG/$RESOURCE index==$INDEX
```

**3. Search Characters**
```bash
http GET $BASE_URL/$LANG/$RESOURCE search==$SEARCH
```

**4. Pagination**
```bash
http GET $BASE_URL/$LANG/$RESOURCE max==$MAX page==$PAGE
```

**5. Limit Results**
```bash
http GET $BASE_URL/$LANG/$RESOURCE max==3
```

**6. Second Resource (Books)**
```bash
http GET $BASE_URL/$LANG/books
```

**7. Random Spell**
```bash
http GET $BASE_URL/$LANG/spells/random
```

**8. 404 – Invalid Endpoint**
```bash
http GET $BASE_URL/$LANG/personajessss
```

**9. Invalid Parameter (Negative max)**
```bash
http GET $BASE_URL/$LANG/$RESOURCE max==-5
```

**10. With Custom Header**
```bash

## HTTPie Syntax Reference
| Syntax | Meaning |
|---|---|
| `Header:Value` | Request header |
| `http GET URL` | GET request |

## Authentication
Therefore, 401 and 403 errors cannot be demonstrated
because no protected endpoints exist.PotterAPI does not require authentication.

| `param==value` | Query parameter |


