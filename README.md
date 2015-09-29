### Requirements

- ProtocolBuffers 2.5.0

### Setup

1. Launch R
    1. Install Rserve if not installed `install.packages("Rserve")`
    1. Start Rserve `library(Rserve); Rserve()`

1. Launch application

### REST API

| URI | Method | Action (Response Code) |
|---|---|---|
| `/predictions`      | GET | return array of all available prediction result ids (200) |
| `/predictions`      | POST | create prediction job using the given feature vector and return location header containing the endpoint `/predictions/<id>` (201) |
| `/predictions`      | PUT | operation not supported (405) |
| `/predictions`      | DELETE | operation not supported (405) |
| `/predictions/<id>` | GET | prediction result with given id (200), prediction not finished (204), id is invalid (404) |
| `/predictions/<id>` | POST | operation not supported (405) |
| `/predictions/<id>` | PUT | operation not supported (405) |
| `/predictions/<id>` | DELETE | operation not supported (405) |

### Send messages via curl

`curl --data-binary "@<file-name>" <interface>:<port>`
