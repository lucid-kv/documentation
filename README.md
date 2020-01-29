---
description: "High performance and distributed KV store accessible through an HTTP API. \U0001F980"
---

# About Lucid ᵏᵛ

## Introduction

Lucid is currently in a development stage but we want to achieve a fast, secure and distributed key-value store accessible through an HTTP API, we also want to propose persistence, encryption, WebSocket streaming, replication and a lot of features.

### Getting Started

Get the latest binary from the [releases](https://github.com/lucid-kv/lucid/releases) page and run these commands:

```text
$ ./lucid init
$ ./lucid --config lucid.yml server
```

Or run a node with Docker, but you need to create a [lucid.yml](https://github.com/lucid-kv/lucid/blob/master/.github/lucid.yml) file locally before.

```text
$ docker pull lucidkv/lucid
$ docker run -v lucid.yml:/etc/lucid/lucid.yml lucidkv/lucid
```

{% page-ref page="getting-started.md" %}

## Quick API Documentation

This is a simple API documentation, Lucid is a REST API, here you can found just CRUD endpoints.

{% api-method method="put" host="https://localhost:7021" path="/api/kv/:key" %}
{% api-method-summary %}
Create or Update
{% endapi-method-summary %}

{% api-method-description %}
This endpoint is used to store and update data.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="key" type="string" required=false %}
Key of the object to store
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=false %}
JWT Token, Needed if authentication is configured
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="raw body" type="string" required=true %}
Raw Body / Json / Binary files
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
The data was successfully updated.
{% endapi-method-response-example-description %}

```
{
  "message": "The specified key was successfully updated."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
The data was successfully created.
{% endapi-method-response-example-description %}

```
  "message": "The specified key was successfully created."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Your are not unauthorized to access to this resource.
{% endapi-method-response-example-description %}

```
Coming soon
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
The key does not exists.
{% endapi-method-response-example-description %}

```
Coming soon
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://localhost:7021" path="/api/kv/:key" %}
{% api-method-summary %}
Get a Key
{% endapi-method-summary %}

{% api-method-description %}
This endpoint get an existing data with his key.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="key" type="string" required=false %}
Key of the object to retrieve
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=false %}
JWT Token, Needed if authentication is configured
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
The raw content of the object, it can be a binary or an ascii text.
{% endapi-method-response-example-description %}

```
Hello world!
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
You are not authorized to access to this resource.
{% endapi-method-response-example-description %}

```
Coming soon
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
The key does not exists.
{% endapi-method-response-example-description %}

```
Coming soon
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://localhost:7021" path="/api/kv/:key" %}
{% api-method-summary %}
Delete a Key
{% endapi-method-summary %}

{% api-method-description %}
This endpoint drop a key if it exists.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="key" type="string" required=false %}
Key of the object to delete
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=false %}
JWT Token, needed if authentication is configured
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
Hello world!
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
Coming soon
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "message": "The specified key does not exists."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Some Use Cases

* Private Keys Storing \(for a wallet by example\)
* IoT: collect and save statistics data
* A distributed cache for an application
* Service Discovery
* Distributed Configuration
* Blob Storage

## Development Credits

Lucid is Written in Rust 🦀, powered by [Clint.Network](https://twitter.com/clint_network) and published under the [MIT License](https://github.com/clintnetwork/lucid/blob/master/LICENSE.md).

| Name / Nickname | Email | Role |
| :--- | :--- | :--- |
| Clint Mourlevat | [me@clint.network](mailto:me@clint.network) | Lucid Founder |
| Jonathan Serra | [jonathan@blocs.fr](mailto:jonathan@blocs.fr) | Core Development |
| CephalonRho | [CephalonRho@gmail.com](mailto:CephalonRho@gmail.com) | Core Development |
| Rigwild | [me@rigwild.dev](mailto:me@rigwild.dev) | Web UI Development |

### Contribute to Lucid

See [CONTRIBUTING.md](https://github.com/lucid-kv/lucid/blob/master/CONTRIBUTING.md) for best practices and instructions on setting up your development environment to work on Lucid.

### Make a Donation

* [![Paypal](https://raw.githubusercontent.com/reek/anti-adblock-killer/gh-pages/images/paypal.png)](https://raw.githubusercontent.com/reek/anti-adblock-killer/gh-pages/images/paypal.png) Paypal: [Donate](http://paypal.me/clintnetwork)
* [![btc](https://raw.githubusercontent.com/reek/anti-adblock-killer/gh-pages/images/bitcoin.png)](https://raw.githubusercontent.com/reek/anti-adblock-killer/gh-pages/images/bitcoin.png) Bitcoin: 3BxEYn4RZ3iYETcFpN7nA6VqCY4Hz1tSUK

{% embed url="https://github.com/lucid-kv" %}

