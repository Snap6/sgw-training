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
this is from the mobile system:
{
    "id": "3",
    "ok": true,
    "rev": "1-622c50a7af0ecb76dff71baa74d13333"
}

1. enable_shared_bucket_access: false, import_docs: false
{
    "id": "135e798ed8c5ed6d9d96222ec4fea75c",
    "ok": true,
    "rev": "1-ad2a21a54435bc855e88a3594813d49a"
}
{
    "_id": "zomatoo",
    "_rev": "3-8ddf2dade557cc0fdef75eed5b0e28a5",
    "click": "to edit nothing here but need that gift card",
    "with JSON": "there are no reserved field names"
}
{
    "_id": "3",
    "_rev": "1-622c50a7af0ecb76dff71baa74d13333",
    "key1": "value1",
    "key2": "value2"
}


2. enable_shared_bucket_access: false, import_docs: true
{
    "id": "ca25cdf47c38db94b2c14f4c928421cc",
    "ok": true,
    "rev": "1-6c499fce246d86f33ea6759fc7c7a007"
}
{
    "_id": "zomatoo",
    "_rev": "3-8ddf2dade557cc0fdef75eed5b0e28a5",
    "click": "to edit nothing here but need that gift card",
    "with JSON": "there are no reserved field names"
}
{
    "_id": "3",
    "_rev": "1-622c50a7af0ecb76dff71baa74d13333",
    "key1": "value1",
    "key2": "value2"
}

3. enable_shared_bucket_access: true, import_docs: false
{
    "id": "a8f1ab19c6c0c327c297ec2afc58f16a",
    "ok": true,
    "rev": "1-e55e3ca339896bb8f563060539ffc865"
}
{
    "_id": "zomatoo",
    "_rev": "3-8ddf2dade557cc0fdef75eed5b0e28a5",
    "click": "to edit nothing here but need that gift card",
    "with JSON": "there are no reserved field names"
}
{
    "_id": "3",
    "_rev": "1-622c50a7af0ecb76dff71baa74d13333",
    "key1": "value1",
    "key2": "value2"
}


4. enable_shared_bucket_access: true, import_docs: true
{
    "db_name": "db1",
    "update_seq": 8,
    "committed_update_seq": 8,
    "instance_start_time": 1737104586619159,
    "compact_running": false,
    "purge_seq": 0,
    "disk_format_version": 0,
    "state": "Online",
    "server_uuid": "813fe4cc7046b2ba0d55bc8821f2b429"
}
{    "_id": "zomatoo",
    "_rev": "3-8ddf2dade557cc0fdef75eed5b0e28a5",
    "click": "to edit nothing here but need that gift card",
    "with JSON": "there are no reserved field names"
}
{
    "_id": "3",
    "_rev": "1-622c50a7af0ecb76dff71baa74d13333",
    "key1": "value1",
    "key2": "value2"
}

```

### Observations
