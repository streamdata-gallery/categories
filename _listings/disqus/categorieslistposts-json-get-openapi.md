---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Categories ListPosts
  description: Categories ListPosts
  termsOfService: https://docs.disqus.com/kb/terms-and-policies/
  version: 1.0.0
host: disqus.com
basePath: api/3.0/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /categories/details.json:
    get:
      summary: Categories Details
      description: Categories Details
      operationId: categories-details
      x-api-path-slug: categoriesdetails-json-get
      parameters:
      - in: query
        name: category
        description: Looks up a category by ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Categories
  /categories/list.json:
    get:
      summary: Categories List
      description: Categories List
      operationId: categories-list
      x-api-path-slug: categorieslist-json-get
      parameters:
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: forum
        description: Looks up a forum by ID (aka short name)
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to asc                         Choices: asc, desc'
        type: string
      - in: query
        name: since_id
        description: Defaults to null
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Categories
  /categories/listPosts.json:
    get:
      summary: Categories ListPosts
      description: Categories ListPosts
      operationId: categories-listposts
      x-api-path-slug: categorieslistposts-json-get
      parameters:
      - in: query
        name: category
        description: Looks up a category by ID
        type: string
      - in: query
        name: cursor
        description: Defaults to null
        type: string
      - in: query
        name: filters
        description: 'Defaults to []                         Valid values are: 1:
          Is_Anonymous 2: Has_Link 3: Has_Low_Rep_Author 4: Has_Bad_Word 5: Is_Flagged
          6: No_Issue 7: Is_Toxic'
        type: string
      - in: query
        name: include
        description: 'Defaults to [  approved]                         Choices: unapproved,
          approved, spam, deleted, flagged, highlighted'
        type: string
      - in: query
        name: limit
        description: Defaults to 25                         Maximum value of 100
        type: string
      - in: query
        name: order
        description: 'Defaults to desc                         Choices: asc, desc'
        type: string
      - in: query
        name: query
        description: Defaults to null
        type: string
      - in: query
        name: related
        description: Defaults to []                         You may specify relations
          to include with your response
        type: string
      - in: query
        name: since
        description: Defaults to null                         Unix timestamp (or ISO
          datetime standard)
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Categories
x-streamrank:
  polling_total_time_average: "0.24"
  polling_size_download_average: "8690.06"
  streaming_total_time_average: "0.15"
  streaming_size_download_average: "4348.7"
  change_yes: "7"
  change_no: "1322"
  time_percentage: "40"
  size_percentage: "50"
  change_percentage: "1"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---