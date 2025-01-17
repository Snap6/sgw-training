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
with revid of 2 cause the import docs is true 

- Review the revision IDs and explain the different values in revision IDs
on the postman : 
first id : 1-622c50a7af0ecb76dff71baa74d13333
first ui : 1-181b726654b000000000000000000000

"revs": [
          "1-622c50a7af0ecb76dff71baa74d13333"
        ]
when accessing it : 
rev cb  : 3-181b72b651f700000000000002000006
revs xattr : [
          "1-622c50a7af0ecb76dff71baa74d13333",
          "2-071a60efac585dd912341b6f7dd07667"
        ]



meanwhile using the ui you basically get the revision id starting with 2 because of the sync-gateway updation results in increments of 2.

so basically when you append or make changes the first id increases and the second part is a hash of the doc 

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
the document both created on the ui and postman have rev id of 1 and 1 but when i call thru the postman it denies 
{
  "meta": {
    "id": "ui",
    "rev": "1-181b71da401d00000000000002000006",
    "expiration": 0,
    "flags": 33554438,
    "type": "json"
  },
  "xattrs": {}
}
{
    "error": "not_found",
    "reason": "Not imported"
}
but on the doc created thru the postman 
{
    "_id": "3",
    "_rev": "1-622c50a7af0ecb76dff71baa74d13333",
    "key1": "value1",
    "key2": "value2"
}
works 


2. enable_shared_bucket_access: false, import_docs: true
{
  "meta": {
    "id": "zomatoo",
    "rev": "1-181b72da660800000000000002000006",
    "expiration": 0,
    "flags": 33554438,
    "type": "json"
  },
  "xattrs": {}
}

when i pull in postman : 
doesn't give the document my man , no xattr as well 



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
