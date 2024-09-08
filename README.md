# Disposable Email Domains List

This repository contains a list of disposable/temporary email domains in various formats for easy integration into different programming languages and frameworks.

## Available Formats

- TypeScript/JavaScript: `temporaryMailList.ts` and `temporaryMailList.js`
- Python: `temporary_mail_list.py`
- Go: `temporary_mail_list.go`
- JSON: `temporary_mail_list.json`
- YAML: `temporary_mail_list.yaml`
- Config: `temporary_mail_list.conf`

## Usage Examples

### TypeScript/JavaScript (Next.js, React, Node.js)

```typescript
import { disposableEmailDomains } from './temporaryMailList';

function isDisposableEmail(email: string): boolean {
  const domain = email.split('@')[1];
  return disposableEmailDomains.includes(domain);
}
```

### Python (Flask, Django)

```python
from temporary_mail_list import disposable_email_domains

def is_disposable_email(email):
    domain = email.split('@')[1]
    return domain in disposable_email_domains
```

### Go

```go
package main

import "strings"

func isDisposableEmail(email string) bool {
    parts := strings.Split(email, "@")
    if len(parts) != 2 {
        return false
    }
    domain := parts[1]
    for _, disposableDomain := range DisposableEmailDomains {
        if domain == disposableDomain {
            return true
        }
    }
    return false
}
```

### Using JSON (for various frameworks)

```javascript
const disposableEmailDomains = require('./temporary_mail_list.json').disposableEmailDomains;

function isDisposableEmail(email) {
  const domain = email.split('@')[1];
  return disposableEmailDomains.includes(domain);
}
```

### Using YAML (for various frameworks)

```python
import yaml

with open('temporary_mail_list.yaml', 'r') as file:
    data = yaml.safe_load(file)
    disposable_email_domains = data['disposableEmailDomains']

def is_disposable_email(email):
    domain = email.split('@')[1]
    return domain in disposable_email_domains
```

Feel free to use the format that best suits your project's needs.

via `jannatkhandev`