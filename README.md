SchmIANA Protocol Parameters
============================

Pre-populated from IANA

```
> curl "https://www.iana.org/protocols" \
  | grep -o "\"[^\"]*\.xhtml[\"#]" \
  | sed -e 's/^"/https:\/\/iana.org/; s/.$//;' \
  | sort | uniq >urls.txt
> for url in `cat urls.txt`; do wget $url; done
```

To request a registration, please submit a pull request.
