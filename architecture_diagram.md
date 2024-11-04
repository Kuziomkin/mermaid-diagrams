```mermaid
---
config:
  layout: dagre
  look: classic
  theme: base
---
    architecture-beta
        group api(cloud)[API]
    
        service db(database)[Database] in api
        service disk1(disk)[Storage] in api
        service disk2(disk)[Storage] in api
        service server(server)[Server] in api
        service bottom_gateway(internet)[Gateway]
        
    
        db:L -- R:server
        disk1:T -- B:server
        disk2:T -- B:db
        bottom_gateway:R -- L:server
```