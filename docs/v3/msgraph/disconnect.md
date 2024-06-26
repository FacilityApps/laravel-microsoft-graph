---
title: Disconnect
---

To disconnect from MsGraph call a **->disconnect()** method.

The disconnect will send a POST request to MsGraph to revoke the connection, in addition, the stored token will be deleted.

```php
MsGraph::disconnect();
```

Typically, you only want to run this is there is a connection, so it makes sense to wrap this in a **->isConnected()** check:

```php
if (MsGraph::isConnected()) {
    MsGraph::disconnect();
}
```