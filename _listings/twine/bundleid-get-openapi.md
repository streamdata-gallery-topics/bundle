---
swagger: "2.0"
x-collection-name: Twine
x-complete: 0
info:
  title: Twine Get a bundle
  description: Get a bundle from a patient's plan.
  version: 7.18.0
host: api.twinehealth.com
basePath: /pub
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /bundle:
    post:
      summary: Create bundle
      description: Create a bundle in a patient's plan
      operationId: createBundle
      x-api-path-slug: bundle-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - Bundle
  /bundle/{id}:
    get:
      summary: Get a bundle
      description: Get a bundle from a patient's plan.
      operationId: fetchBundle
      x-api-path-slug: bundleid-get
      parameters:
      - in: path
        name: id
        description: Bundle identifier
      responses:
        200:
          description: OK
      tags:
      - Wearables
      - Bundle
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---