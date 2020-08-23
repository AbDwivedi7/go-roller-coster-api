# go-roller-coaster-api

> A simple REST API

* No third-party packages/dependencies
* Used in the "How to use curl as an HTTP Client" video
* Building of this API available as a video (coming soon)

## Requirements

To be able to show the desired features of curl this REST API must match a few
requirements:

* [x] `GET   /api/coasters` returns list of coasters as JSON
* [x] `GET   /api/coasters/{id}` returns details of specific coaster as JSON
* [x] `POST  /api/coasters` accepts a new coaster to be added
* [x] `POST  /api/coasters` returns status 415 if content is not `application/json`
* [x] `GET   /api/admin` requires basic auth
* [x] `GET   /api/coasters/random` redirects (Status 302) to a random coaster

### Data Types

A coaster object should look like this:
```json
{
  "id": "someid",
  "name": "name of the coaster",
  "inPark": "the amusement park the ride is in",
  "manufacturer": "name of the manufacturer",
  "height": 27,
}
```

### Persistence

There is no persistence, a temporary in-mem story is fine.
