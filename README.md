# README

## About

This is the official Wails Vue template.

You can configure the project by editing `wails.json`. More information about the project settings can be found
here: https://wails.io/docs/reference/project-config

## Live Development

To run in live development mode, run `wails dev` in the project directory. This will run a Vite development
server that will provide very fast hot reload of your frontend changes. If you want to develop in a browser
and have access to your Go methods, there is also a dev server that runs on http://localhost:34115. Connect
to this in your browser, and you can call your Go code from devtools.

## Building

To build a redistributable, production mode package, use `wails build`.

## Requirements

```bash
# Ubuntu 22.04
go install github.com/wailsapp/wails/v2/cmd/wails@latest

vim ~/.bashrc
# + export PATH=$PATH:$HOME/go/bin

source ~/.bashrc

wails doctor
```

Init project VueJS

```bash
wails init -n go-wails-vue-hello-world -t vue
```

Execute the following command to run the code:

```bash
go run main.go
```

Formatting: For better readability, use the go fmt command to automatically format your code:

```bash
go fmt main.go
```

Building a Binary: To create a standalone executable file, use the go build command:

```bash
go build -o hello main.go
```

This will create an executable file named hello in your project directory. You can run it directly without the go run command.

Using Modules: For larger projects, consider using Go modules for dependency management.
