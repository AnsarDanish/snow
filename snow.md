# ServiceNow Interview Notes

## 1. What is a Business Rule?
- A Business Rule is a server-side script that executes when a record is inserted, updated, deleted, or queried.  
- It is used to enforce rules, manipulate data, and trigger events.

### Example:
```javascript
(function executeRule(current, previous /*null when async*/) {
    if (current.active == true && previous.active == false) {
        gs.addInfoMessage("Record has been activated!");
    }
})(current, previous);


