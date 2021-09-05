<h3 align="center">Elasticsearch learning</h3>

---

<p align="center"> Project created during my study of elasticsearch.
Follow the steps necessary to start your knowledge of elasticsearch.
    <br> 
</p>

## 📝 Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Commands](#commands)

## 🧐 About <a name = "about"></a>

The following steps will teach you what you need to start working with Elasticsearch.
Starting with installation, basic commands as well as advanced commands.

## 🏁 Getting Started <a name = "getting_started"></a>

These instructions will show you installing elasticsearch (7.4.2) and Kibana (7.4.2) 

### Download

To install Elastichsearch download the file <a href="https://www.elastic.co/pt/downloads/past-releases/elasticsearch-7-4-2" target="_blank">here</a>.
To install Kibana download the file <a href="https://www.elastic.co/pt/downloads/past-releases/kibana-7-4-2" target="_blank">here</a>.

### 🔧 Checking the Elasticsearch

Open the following url in your browser: <a href="http://localhost:9200/" target="_blank">http://localhost:9200/</a>

### 🔧 Checking the Kibana

Open the following url in your browser: <a href="http://localhost:9200/" target="_blank">http://localhost:9200/</a>

## 🚀 Commands <a name = "commands"></a>

Below is the list of commands for learning elasticsearch, the commands must be executed in kibana in the dev tools section.

### Checking index

This command returns status by html code

```
HEAD people
```
Return
```
404 - Not Found
```
### Insert data

This command inserts a document on people index

```
POST people/_doc/
{
    "name": "João Silva",
    "interests": ["futebol", "música", "cinema"],
    "genre": "masculino",
    "city": "São Paulo",
    "state": "SP",
    "country": "Brasil"
}
```

Command to insert by entering an id

```
POST people/_doc/1
{
    "name": "Maria Souza",
    "interests": ["música", "atletismo"],
    "genre": "feminino",
    "city": "Rio de Janeiro",
    "state": "RJ",
    "country": "Brasil"
}
```
### Searching
Command retrieves total records
```
GET people/_count
```
Command search by ID
```
GET people/_doc/1
```
Command search by all attibutes
```
GET people/_search?q=atletismo
```
Command search by specific attribute
### Update data
Command to update
```
POST people/_update/1
{
  "doc": {
    "name": "Maria Silva"
  }
}
```
### Delete data
Command to delete
```
DELETE people/_doc/1
```
## ✍️ Authors <a name = "authors"></a>

- [@jonatascp](https://github.com/jonatascp)
