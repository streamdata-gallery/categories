---
swagger: "2.0"
x-collection-name: Etsy
x-complete: 0
info:
  title: Etsy Get Taxonomy Categories Tag Subtag
  description: Retrieves children of a second-level Category by tag and subtag.
  version: 1.0.0
host: openapi.etsy.com
basePath: /v2/private/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /categories/{tag}:
    get:
      summary: Get Categories Tag
      description: Retrieves a top-level Category by tag.
      operationId: getCategoriesTag
      x-api-path-slug: categoriestag-get
      parameters:
      - in: path
        name: tag
      responses:
        200:
          description: OK
      tags:
      - Categories
      - Tag
  /categories/{tag}/{subtag}:
    get:
      summary: Get Categories Tag Subtag
      description: Retrieves a second-level Category by tag and subtag.
      operationId: getCategoriesTagSubtag
      x-api-path-slug: categoriestagsubtag-get
      parameters:
      - in: path
        name: subtag
      - in: path
        name: tag
      responses:
        200:
          description: OK
      tags:
      - Categories
      - Tag
      - Subtag
  /categories/{tag}/{subtag}/{subsubtag}:
    get:
      summary: Get Categories Tag Subtag Subsubtag
      description: Retrieves a third-level Category by tag, subtag and subsubtag.
      operationId: getCategoriesTagSubtagSubsubtag
      x-api-path-slug: categoriestagsubtagsubsubtag-get
      parameters:
      - in: path
        name: subsubtag
      - in: path
        name: subtag
      - in: path
        name: tag
      responses:
        200:
          description: OK
      tags:
      - Categories
      - Tag
      - Subtag
      - Subsubtag
  /taxonomy/categories:
    get:
      summary: Get Taxonomy Categories
      description: Retrieves all top-level Categories.
      operationId: getTaxonomyCategories
      x-api-path-slug: taxonomycategories-get
      responses:
        200:
          description: OK
      tags:
      - Taxonomy
      - Categories
  /taxonomy/categories/{tag}:
    get:
      summary: Get Taxonomy Categories Tag
      description: Retrieves children of a top-level Category by tag.
      operationId: getTaxonomyCategoriesTag
      x-api-path-slug: taxonomycategoriestag-get
      parameters:
      - in: path
        name: tag
      responses:
        200:
          description: OK
      tags:
      - Taxonomy
      - Categories
      - Tag
  /taxonomy/categories/{tag}/{subtag}:
    get:
      summary: Get Taxonomy Categories Tag Subtag
      description: Retrieves children of a second-level Category by tag and subtag.
      operationId: getTaxonomyCategoriesTagSubtag
      x-api-path-slug: taxonomycategoriestagsubtag-get
      parameters:
      - in: path
        name: subtag
      - in: path
        name: tag
      responses:
        200:
          description: OK
      tags:
      - Taxonomy
      - Categories
      - Tag
      - Subtag
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