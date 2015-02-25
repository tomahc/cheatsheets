#### self-signed certificate
```
openssl req \
  -x509 -nodes -days 365 \
  -newkey rsa:1024 -keyout mycert.pem -out mycert.pem
```

#### with subject information
```
openssl req \
  -x509 -nodes -days 365 \
  -subj '/C=US/ST=Oregon/L=Portland/CN=www.example.com' \
  -newkey rsa:1024 -keyout mycert.pem -out mycert.pem
```

#### cert request
```openssl req -new -key mykey.pem -out myreq.pem```

#### with subject information
```
openssl req \
  -new -newkey rsa:1024 -nodes \
  -subj '/CN=www.domain.com/O=My Dom, Inc./C=US/ST=Oregon/L=Portland' \
  -keyout mykey.pem -out myreq.pem
```
  
#### verify signature
```openssl req -in myreq.pem -noout -verify -key mykey.pem```

#### verify certificate
```openssl verify cert.pem```

#### create rsa key
```openssl genrsa -out mykey.pem 1024```

#### create public rsa key
```openssl rsa -in mykey.pem -pubout```

#### digest
```
openssl dgst -sha1 filename
openssl dgst -md5 filename
sha1sum filename
md5sum filename
```

#### signing a digest
```
openssl dgst -sha1 \
  -sign mykey.pem
  -out foo-1.23.tar.gz.sha1 \
  foo-1.23.tar.gz
```
  
#### verify signed digest`
```
openssl dgst -sha1 \
  -verify pubkey.pem \
  -signature foo-1.23.tar.gz.sha1 \
  foo-1.23.tar.gz
```
  
#### encrypt a file
```openssl enc -aes-256-cbc -salt -in file.txt -out file.enc```

#### get crt information
```openssl x509 -in crt -noout -text```
