# go-wasm
Go Web Assembly

Two files need to be copied from `$GOROOT/misc/wasm`
* `wasm_exec.html`
* `wasm_exec.js`

After copying these files, in `wasm_exec.html` rename `test.wasm` to `lib.wasm`
Then rename the file itself from `wasm_exec.html` > `index.html`

A Go program is compiled into a Web Assembly `lib.wasm` file.
By default on my windows gaming PC `GOARCH=amd64`, this needs to be changed to `wasm`
Also `GOOS=windows`, this needs to be changed to `js`
Can do this in one command
`GOARCH=wasm GOOS=js go build -o lib.wasm main.go`

Then `go run server.go` navigate to `localhost:8080` 
This will display a run button. When clicked the button will output `Hello world` to the console.

