# covalent-data
Need mock API? Use covalent-data.
Configuration is simple!
## Golang based mock api server

Latest install docs and user guide can be found [here](https://www.gitbook.com/book/ilsiepotamus/covalent-data).

### Getting started
#### go
To run from source or to create your own executables, you must first install [Go](https://golang.org/doc/install).

1. Pull down this repository into your $GOROOT src folder
2. cd into this repo and `go get`
3. `go run server.go`
4. The `/schema` directory and the `/datum` directory must be in the root of this repo.

#### npm
The covalent-data CLI is available to download as a package in the [npm repository](https://www.npmjs.com/package/@covalent/data).

1. `npm install @covalent/data -g`
2. `covalent-data`

#### docker
To run from docker:

1. Install [Docker Engine](https://docs.docker.com/engine/installation/).
2. Pull down this repo and `cd` into it.
3. `docker build -t covalent-data .`
4. `docker run -p 8080:8080 --name covalent-data covalent-data`
5. To stop- `docker stop covalent-data`

#### covalent-quickstart
covalent-data is included in the [covalent-quickstart](https://github.com/Teradata/covalent-quickstart) repo.

1. Pull down the latest covalent-quickstart repo.
2. `npm install`
3. `npm run start-api` (`npm run stop-api` to stop the API server)
4. `ng serve` and go to http://localhost:42001

#### API configuration (short)
In mock-api/config are located "datum" and "schemas"

"datum" - Here you create files (the name is important!). In them, write the values.

`Foods`
`Drinks`
`Drags` etc


"schemas" - The file has a .yaml extension. Here the table itself is formed.

---
initial_entries: 1
randomize: false
labels: {{.all_labels}}
...


initial_entries - number of records generated

randomize - If true, then randomly will take data from the datum file

labels - Exist file with name "labels" in datum. Using {{.}} is important.

Pay attention to the boundary lines (they are different)!
