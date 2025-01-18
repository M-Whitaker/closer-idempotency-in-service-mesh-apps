# Idempotency in Service Mesh: for Resiliency of Fog-Native Applications in Multi-Domain Edge-to-Cloud Ecosystems

## Idempotency DataStore Schema

```yaml
apiVersion: idempotency.example.com/v1alpha1
kind: DatastoreSchema
metadata:
  name: schema
spec:
  fields:
    - name: id
      type: uuid
      constraints:
        - "not null"
        - "primary key"
    - name: service_name
      type: string
      constraints:
        - "not null"
        - "primary key"
    - name: cluster_id
      type: string
      constraints:
        - "not null"
    - name: req_checksum
      type: string
      constraints:
        - "not null"
    - name: res_body
      type: json
    - name: status_code
      type: integer
      constraints:
        - "not null"
    - name: created date
      type: timestamp
      constraints:
        - "not null"
        - "default"
        - "current_timestamp"
    - name: completer downstream resource
      type: string
    - name: completed_at
      type: timestamp
```
