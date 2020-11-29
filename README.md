# Web worker example

This repo is an example of a web worker in action. The use case is a JPEG fetcher which transforms the response into a blob, then into an `ArrayBuffer`, then the EXIF data is extracted. There are two states denoted by two tags:

1. `without-worker`, which does all this work on the main thread.
2. `with-worker`, which moves the fetching, EXIF extraction, and markup construction into a web worker.

To use this repo, clone, `npm install`, and then spin up the local server via `npm start`. Once the server is started, it will be available at [http://localhost:8080](http://localhost:8080).
