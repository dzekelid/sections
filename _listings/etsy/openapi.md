swagger: "2.0"
x-collection-name: Etsy
x-complete: 1
info:
  title: Etsy
  description: bring-etsys-handmade-marketplace-and-community-into-your-apps-
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