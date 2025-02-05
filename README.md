
<div align="center">
<img src="https://github.com/quarkiverse/quarkus-ngrok/blob/main/docs/modules/ROOT/assets/images/quarkus.svg" width="67" height="70" ><img src="https://github.com/quarkiverse/quarkus-ngrok/blob/main/docs/modules/ROOT/assets/images/plus-sign.svg" height="70" ><img src="https://github.com/quarkiverse/quarkus-ngrok/blob/main/docs/modules/ROOT/assets/images/ngrok.svg" height="70" >

# Quarkus Ngrok
</div>
<br>

[![Version](https://img.shields.io/maven-central/v/io.quarkiverse.ngrok/quarkus-ngrok?logo=apache-maven&style=flat-square)](https://search.maven.org/artifact/io.quarkiverse.ngrok/quarkus-ngrok)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=flat-square)](https://opensource.org/licenses/Apache-2.0)
[![Build](https://github.com/quarkiverse/quarkus-ngrok/actions/workflows/build.yml/badge.svg)](https://github.com/quarkiverse/quarkus-ngrok/actions/workflows/build.yml)


## Purpose

This Quarkus extension integrates [ngrok](https://ngrok.com/) into Quarkus Dev Mode thus allowing users to expose their application to the public internet while they are still developing it.

NOTE: The extension has absolutely no impact on the production Quarkus application

## Compatibility

| Quarkus | Quarkus Ngrok |
|---------|---------------|
| 2.x     | 0.x           |
| 3.x     | 1.x           |

## Usage

1. Add the extension to the application's dependencies `./mvnw quarkus:add-extension -Dextensions="io.quarkiverse.ngrok:quarkus-ngrok"`

2. Start Quarkus in Dev Mode with the following configuration property `quarkus.ngrok.enabled=true`. It is also advised for users to sign up for a free ngrok account and use the obtained token using `quarkus.ngrok.auth-token=sometoken` 

3. A short while after the application has started, you should see something in the application logs like:

```bash
ngrok is running and its web interface can be accessed at: 'http://localhost:4040'
The application can be accessed publicly over the internet using: 'http://4f59-68-81-186-238.ngrok-free.app'
```

4. Use the `.ngrok-free.app` URL to access the running application from the public internet
