# Email header analysis

Analyse email headers for origin tracing:

```python
import email
from email.header import decode_header

def analyze_email(path):
    with open(path, 'r') as f:
        msg = email.message_from_file(f)
    
    print("=== Email Header Analysis ===")
    for header in ['From', 'To', 'Subject', 'Date', 'Received']:
        values = msg.get_all(header, [])
        for value in values:
            decoded = decode_header(value)
            print(f"{header}: {' '.join(str(t[0]) for t in decoded)}")
    
    print("\n=== Routing Information ===")
    for received in msg.get_all('Received', []):
        print(received)
```