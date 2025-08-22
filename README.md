# RAiD resolver

## Introduction

This proof of concept RAiD resolver uses the HAProxy reverse proxy to send RAiD resolution requests to the Handle server.

If the Handle server cannot resolve the Handle and returns a 404 error, HAProxy intercepts the error and displays its own
error page, as defined in `ha-proxy-config/errorfiles/404.http`.

## Give it a spin

1. Clone this repo
2. `docker compose up`
3. Try to visit some URLs
    * Valid RAiD: [http://localhost:8080/10.26312/db3c5429]
    * Invalid RAiD: [http://localhost:8080/10.26312/foo] 