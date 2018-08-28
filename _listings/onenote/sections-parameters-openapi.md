---
swagger: "2.0"
x-collection-name: OneNote
x-complete: 0
info:
  title: One Note Parameters Sections
  description: Parameters sections.
  version: 1.0.0
host: www.onenote.com
basePath: /api/v1.0/me/notes/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /sections/{sectionId}:
    get:
      summary: Get Sections Sectionid
      description: Returns a specific section.
      operationId: getSectionsSection
      x-api-path-slug: sectionssectionid-get
      parameters:
      - in: query
        name: expand
        description: The navigation properties (parentNotebook, or parentSectionGroup)
          to return inline in the response
      - in: path
        name: sectionId
        description: Specifies the specific Section
      - in: query
        name: select
        description: The properties to return
      responses:
        200:
          description: OK
      tags:
      - Sections
      - SectionId
    parameters:
      summary: Parameters Sections Sectionid
      description: Parameters sections sectionid.
      operationId: parametersSectionsSection
      x-api-path-slug: sectionssectionid-parameters
      responses:
        200:
          description: OK
      tags:
      - Sections
      - SectionId
  /sections/:
    get:
      summary: Get Sections
      description: Returns a collection of sections.
      operationId: getSections
      x-api-path-slug: sections-get
      parameters:
      - in: query
        name: count
        description: true, to return the number of entities in the collection
      - in: query
        name: expand
        description: The navigation properties (parentNotebook or parentSectionGroup)
          to return inline in the response
      - in: query
        name: filter
        description: The filter for the query
      - in: query
        name: orderby
        description: The property to order by
      - in: query
        name: select
        description: The properties to return
      - in: query
        name: skip
        description: The number of entities to skip in the result set
      - in: query
        name: top
        description: The number of entities to return from the result set
      responses:
        200:
          description: OK
      tags:
      - Sections
    parameters:
      summary: Parameters Sections
      description: Parameters sections.
      operationId: parametersSections
      x-api-path-slug: sections-parameters
      responses:
        200:
          description: OK
      tags:
      - Sections
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