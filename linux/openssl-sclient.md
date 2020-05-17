# Using OpenSSL

There are lots of different options for using the s_client command.

To check the expiration date of a website from the command line:
```bash
echo 'Q' | openssl s_client -connect ml.umd.edu:443 2>/dev/null | openssl x509 -noout -dates
```

The `echo 'Q'` makes the comand return instead of just hanging.
