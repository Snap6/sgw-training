# Tasks

## Task 1

### Description

- Setup SGW using setup 1
done 
- Use Postman to check if SGW is working (use Admin PORT)
yessir


### Observations

## Task 2

### Description

- Setup SGW using setup 2 
```
WARN[0000] /Users/ramesh.d/Documents/Projects/sgw-training/docker-compose.yml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion 
[+] Running 1/0
 ✔ Container cb-sgw  Running 
```™
- Create a Database using Postman
created a new database updated the basic auth
- Create a Document using Postman
yessir done by your command
- Get the document using Postman
yessir done , modified it as well

### Observations

## Task 3

### Description

- This task continues from the previous task
- Create a dummy document from CB UI jsut added it as defauult
ddone it 
- Get the document contents using Postman
yes done 
0.0.0.0:4985/db1/zomatoo
- Delete the document using Postman
done conflict arises

### Observations

## Task 4

### Description

- Create a document from Couchbase Server UI
done it's called zomatooooo
- Review the revision IDs and explain the different values in revision IDs
first id : 1-6c09ee187cece3ab2da390476ac6b48f
second id : 2-bfa741a85dcfe111c1b0945078f2b049
third id : 3-8ddf2dade557cc0fdef75eed5b0e28a5

so basically when you append or make changes the first id increases and the second part is a hash or somethiing 

### Observations

## Task 5

### Description

- Test the following configurations of SGW database:

```
1. enable_shared_bucket_access: false, import_docs: false
2. enable_shared_bucket_access: false, import_docs: true
3. enable_shared_bucket_access: true, import_docs: false
4. enable_shared_bucket_access: true, import_docs: true
```

### Observations
