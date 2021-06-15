# :zap: Golang Http API

* Golang JSON REST API using [Gorilla Mux](https://github.com/gorilla/mux) as the HTTP router and URL matcher. Tutorial code from [Devstackr, Youtube video: Build a RESTful HTTP API in Golang w/ Mux](https://www.youtube.com/watch?v=HmiybuiEZI4&t=175s)
* **Note:** to open web links in a new window use: _ctrl+click on link_

![GitHub repo size](https://img.shields.io/github/repo-size/AndrewJBateman/golang-http-api?style=plastic)
![GitHub pull requests](https://img.shields.io/github/issues-pr/AndrewJBateman/golang-http-api?style=plastic)
![GitHub Repo stars](https://img.shields.io/github/stars/AndrewJBateman/golang-http-api?style=plastic)
![GitHub last commit](https://img.shields.io/github/last-commit/AndrewJBateman/golang-http-api?style=plastic)

## :page_facing_up: Table of contents

* [:zap: Golang Http API](#zap-golang-http-api)
  * [:page_facing_up: Table of contents](#page_facing_up-table-of-contents)
  * [:books: General info](#books-general-info)
  * [:camera: Screenshots](#camera-screenshots)
  * [:signal_strength: Technologies](#signal_strength-technologies)
  * [:floppy_disk: Setup](#floppy_disk-setup)
  * [:computer: Code Examples](#computer-code-examples)
  * [:cool: Features](#cool-features)
  * [:clipboard: Status & To-do list](#clipboard-status--to-do-list)
  * [:clap: Inspiration](#clap-inspiration)
  * [:file_folder: License](#file_folder-license)
  * [:envelope: Contact](#envelope-contact)

## :books: General info

* Go’s default request handler signature is `func (w http.ResponseWriter, r *http.Request)`

## :camera: Screenshots

![techData screen print](./img/post.png)

## :signal_strength: Technologies

* [go version go1.14 windows/amd64](https://golang.org/) programming language
* [Gorilla web toolkit](http://www.gorillatoolkit.org/pkg/mux) HTTP request multiplexer

## :floppy_disk: Setup

* You need to [download & install Go](https://golang.org/dl/)
* [Set the path of your workspace location in your platform Environment Variables](https://github.com/golang/go/wiki/SettingGOPATH)
* Install [Go in Visual Studio](https://code.visualstudio.com/docs/languages/go)
* Install the Go toolchain in Visual Studio

## :computer: Code Examples

* function to get a post using the Gorilla mux, with pointer type *http.Request

```golang
func getPost(w http.ResponseWriter, r *http.Request) {
  // get the ID of the post from the route parameter
  // golang method strconv.Atoi is equivalent to ParseInt(s, 10, 0), converted to type int.
  ar idParam string = mux.Vars(r)["id"]
  id, err := strconv.Atoi(idParam)
  if err != nil {
    // there was an error
    w.WriteHeader(400)
    w.Write([]byte("ID could not be converted to integer"))
    return
  }
```

## :cool: Features

* [Method to delete post using append slice-manipulation](https://github.com/golang/go/wiki/SliceTricks#delete)

## :clipboard: Status & To-do list

* Status: Working
* To-do: Nothing

## :clap: Inspiration

* All code from [Devstackr, Youtube video: Build a RESTful HTTP API in Golang w/ Mux](https://www.youtube.com/watch?v=HmiybuiEZI4&t=175s)
* [Hugo Johnsson: Medium article REST-API with Golang and Mux](https://medium.com/@hugo.bjarred/rest-api-with-golang-and-mux-e934f581b8b5)
* [Go Web Examples: Routing (using gorilla/mux)](https://gowebexamples.com/routes-using-gorilla-mux/)

## :file_folder: License

* This project is licensed under the terms of the MIT license.

## :envelope: Contact

* Repo created by [ABateman](https://github.com/AndrewJBateman), email: gomezbateman@yahoo.com
