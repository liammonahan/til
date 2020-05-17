# Creating Files of a Certain Size

Today I learned how to create a random file of arbitrary size:

```bash
openssl rand -out sample.txt -base64 $(( 2**28 ))
```
