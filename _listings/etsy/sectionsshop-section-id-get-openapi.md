---
swagger: "2.0"
x-collection-name: Etsy
x-complete: 0
info:
  title: Etsy Get Sections Shop Section
  description: Retrieves a ShopSection by id.
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
  /shops/{shop_id}/sections:
    get:
      summary: Get Shops Shop Sections
      description: Retrieves a set of ShopSection objects associated to a Shop.
      operationId: getShopsShopSections
      x-api-path-slug: shopsshop-idsections-get
      parameters:
      - in: path
        name: shop_id
      responses:
        200:
          description: OK
      tags:
      - Shops
      - Shop
      - Sections
  /sections/{shop_section_id}:
    get:
      summary: Get Sections Shop Section
      description: Retrieves a ShopSection by id.
      operationId: getSectionsShopSection
      x-api-path-slug: sectionsshop-section-id-get
      parameters:
      - in: path
        name: shop_section_id
      responses:
        200:
          description: OK
      tags:
      - Sections
      - Shop
      - Section
    put:
      summary: Put Sections Shop Section
      description: Updates a ShopSection with the given id.
      operationId: putSectionsShopSection
      x-api-path-slug: sectionsshop-section-id-put
      parameters:
      - in: query
        name: rank
      - in: path
        name: shop_section_id
      - in: query
        name: title
      - in: query
        name: user_id
      responses:
        200:
          description: OK
      tags:
      - Sections
      - Shop
      - Section
    delete:
      summary: Delete Sections Shop Section
      description: Deletes the ShopSection with the given id.
      operationId: deleteSectionsShopSection
      x-api-path-slug: sectionsshop-section-id-delete
      parameters:
      - in: path
        name: shop_section_id
      responses:
        200:
          description: OK
      tags:
      - Sections
      - Shop
      - Section
  /sections:
    post:
      summary: Post Sections
      description: Creates a new ShopSection.
      operationId: postSections
      x-api-path-slug: sections-post
      parameters:
      - in: query
        name: title
      - in: query
        name: user_id
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