---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Courses API List group categories for a context
  description: List group categories for a context.
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /courses/{course_id}/group_categories:
    get:
      summary: List group categories for a context
      description: List group categories for a context.
      operationId: list-group-categories-for-a-context
      x-api-path-slug: coursescourse-idgroup-categories-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Group
      - Categories
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