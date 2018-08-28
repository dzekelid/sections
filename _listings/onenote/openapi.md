swagger: "2.0"
x-collection-name: OneNote
x-complete: 1
info:
  title: One Note
  description: easily-capture-content-into-onenote-with-this-rest-api-
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
  /sectionGroups/{sectionGroupId}/sections:
    get:
      summary: Get Sectiongroups Sectiongroupid Sections
      description: Returns a collection of sections within a specific section group.
      operationId: getSectiongroupsSectiongroupSections
      x-api-path-slug: sectiongroupssectiongroupidsections-get
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
      - in: path
        name: sectionGroupId
        description: Specifies the section group
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
      - SectionGroups
      - SectionGroupId
      - Sections
    parameters:
      summary: Parameters Sectiongroups Sectiongroupid Sections
      description: Parameters sectiongroups sectiongroupid sections.
      operationId: parametersSectiongroupsSectiongroupSections
      x-api-path-slug: sectiongroupssectiongroupidsections-parameters
      responses:
        200:
          description: OK
      tags:
      - SectionGroups
      - SectionGroupId
      - Sections
    post:
      summary: Post Sectiongroups Sectiongroupid Sections
      description: Post sectiongroups sectiongroupid sections.
      operationId: postSectiongroupsSectiongroupSections
      x-api-path-slug: sectiongroupssectiongroupidsections-post
      parameters:
      - in: query
        name: Content-Type
        description: 'Required: The type of content being sent'
      - in: path
        name: sectionGroupId
        description: Specifies the section group
      responses:
        200:
          description: OK
      tags:
      - SectionGroups
      - SectionGroupId
      - Sections
  /notebooks/{notebookId}/sections:
    get:
      summary: Get Notebooks Notebookid Sections
      description: Returns a collection of sections within a specific notebook.
      operationId: getNotebooksNotebookSections
      x-api-path-slug: notebooksnotebookidsections-get
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
      - in: path
        name: notebookId
        description: Specifies the notebook
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
      - Notebooks
      - NotebookId
      - Sections
    post:
      summary: Post Notebooks Notebookid Sections
      description: Creates a new section in a specific notebook.
      operationId: postNotebooksNotebookSections
      x-api-path-slug: notebooksnotebookidsections-post
      parameters:
      - in: header
        name: Content-Type
        description: 'Required: indicates type of content being sent'
      - in: query
        name: Content-Type
        description: 'Required: indicates type of content being sent'
      - in: path
        name: notebookId
        description: Specifies the notebook
      responses:
        200:
          description: OK
      tags:
      - Notebooks
      - NotebookId
      - Sections
    parameters:
      summary: Parameters Notebooks Notebookid Sections
      description: Parameters notebooks notebookid sections.
      operationId: parametersNotebooksNotebookSections
      x-api-path-slug: notebooksnotebookidsections-parameters
      responses:
        200:
          description: OK
      tags:
      - Notebooks
      - NotebookId
      - Sections
  /sections/{sectionId}/pages:
    get:
      summary: Get Sections Sectionid Pages
      description: Get the pages (metadata) in the specified section.
      operationId: getSectionsSectionPages
      x-api-path-slug: sectionssectionidpages-get
      parameters:
      - in: query
        name: count
        description: true, to return the number of entities in the collection
      - in: query
        name: expand
        description: The navigation properties (parentNotebook or parentSection) to
          return inline in the response
      - in: query
        name: filter
        description: The filter for the query
      - in: query
        name: orderby
        description: The property to order by
      - in: query
        name: pagelevel
        description: true, to return the level and order properties for pages
      - in: query
        name: search
        description: The term or phrase to search for
      - in: path
        name: sectionId
        description: Specifies the section that contains the pages
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
      - SectionId
      - Pages
    post:
      summary: Post Sections Sectionid Pages
      description: Creates a new page in a specific section.
      operationId: postSectionsSectionPages
      x-api-path-slug: sectionssectionidpages-post
      parameters:
      - in: header
        name: Content-Type
        description: 'Required: indicates type of content sent'
      - in: query
        name: Content-Type
        description: 'Required: indicates type of content sent'
      - in: path
        name: sectionId
        description: Specifies the section to create the page in
      responses:
        200:
          description: OK
      tags:
      - Sections
      - SectionId
      - Pages
    parameters:
      summary: Parameters Sections Sectionid Pages
      description: Parameters sections sectionid pages.
      operationId: parametersSectionsSectionPages
      x-api-path-slug: sectionssectionidpages-parameters
      responses:
        200:
          description: OK
      tags:
      - Sections
      - SectionId
      - Pages
  /sectionGroups/{sectionGroupId}/sectionGroups:
    get:
      summary: Get Sectiongroups Sectiongroupid Sectiongroups
      description: Returns a collection of section groups within a specific section
        group.
      operationId: getSectiongroupsSectiongroupSectiongroups
      x-api-path-slug: sectiongroupssectiongroupidsectiongroups-get
      parameters:
      - in: query
        name: count
        description: true, to return the number of entities in the collection
      - in: query
        name: expand
        description: The navigation properties (sections, sectionGroups, parentNotebook,
          or parentSectionGroup) to return inline in the response
      - in: query
        name: filter
        description: The filter for the query
      - in: query
        name: orderby
        description: The property to order by
      - in: path
        name: sectionGroupId
        description: Specifies the section group
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
      - SectionGroups
      - SectionGroupId
      - SectionGroups
    parameters:
      summary: Parameters Sectiongroups Sectiongroupid Sectiongroups
      description: Parameters sectiongroups sectiongroupid sectiongroups.
      operationId: parametersSectiongroupsSectiongroupSectiongroups
      x-api-path-slug: sectiongroupssectiongroupidsectiongroups-parameters
      responses:
        200:
          description: OK
      tags:
      - SectionGroups
      - SectionGroupId
      - SectionGroups
    post:
      summary: Post Sectiongroups Sectiongroupid Sectiongroups
      description: Post sectiongroups sectiongroupid sectiongroups.
      operationId: postSectiongroupsSectiongroupSectiongroups
      x-api-path-slug: sectiongroupssectiongroupidsectiongroups-post
      parameters:
      - in: query
        name: Content-Type
        description: 'Required: The type of content being sent'
      - in: path
        name: sectionGroupId
        description: Specifies the section group
      responses:
        200:
          description: OK
      tags:
      - SectionGroups
      - SectionGroupId
      - SectionGroups
  /sectionGroups/{sectionGroupId}:
    get:
      summary: Get Sectiongroups Sectiongroupid
      description: Returns a specific section group object.
      operationId: getSectiongroupsSectiongroup
      x-api-path-slug: sectiongroupssectiongroupid-get
      parameters:
      - in: query
        name: expand
        description: The navigation properties (sections, sectionGroups, parentNotebook,
          or parentSectionGroup) to return inline in the response
      - in: path
        name: sectionGroupId
        description: Specifies the specific section group
      - in: query
        name: select
        description: The properties to return
      responses:
        200:
          description: OK
      tags:
      - SectionGroups
      - SectionGroupId
    parameters:
      summary: Parameters Sectiongroups Sectiongroupid
      description: Parameters sectiongroups sectiongroupid.
      operationId: parametersSectiongroupsSectiongroup
      x-api-path-slug: sectiongroupssectiongroupid-parameters
      responses:
        200:
          description: OK
      tags:
      - SectionGroups
      - SectionGroupId
  /sectionGroups/:
    get:
      summary: Get Sectiongroups
      description: Returns a collection of section groups.
      operationId: getSectiongroups
      x-api-path-slug: sectiongroups-get
      parameters:
      - in: query
        name: count
        description: true, to return the number of entities in the collection
      - in: query
        name: expand
        description: The navigation properties (sections, sectionGroups, parentNotebook,
          or parentSectionGroup) to return inline in the response
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
      - SectionGroups
    parameters:
      summary: Parameters Sectiongroups
      description: Parameters sectiongroups.
      operationId: parametersSectiongroups
      x-api-path-slug: sectiongroups-parameters
      responses:
        200:
          description: OK
      tags:
      - SectionGroups
  /notebooks/{notebookId}/sectiongroups:
    get:
      summary: Get Notebooks Notebookid Sectiongroups
      description: Returns a collection of section groups within a specific notebook.
      operationId: getNotebooksNotebookSectiongroups
      x-api-path-slug: notebooksnotebookidsectiongroups-get
      parameters:
      - in: query
        name: count
        description: true, to return the number of entities in the collection
      - in: query
        name: expand
        description: The navigation properties (sections, sectionGroups, parentNotebook,
          or parentSectionGroup) to return inline in the response
      - in: query
        name: filter
        description: The filter for the query
      - in: path
        name: notebookId
        description: Specifies the notebook
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
      - Notebooks
      - NotebookId
      - Sectiongroups
    parameters:
      summary: Parameters Notebooks Notebookid Sectiongroups
      description: Parameters notebooks notebookid sectiongroups.
      operationId: parametersNotebooksNotebookSectiongroups
      x-api-path-slug: notebooksnotebookidsectiongroups-parameters
      responses:
        200:
          description: OK
      tags:
      - Notebooks
      - NotebookId
      - Sectiongroups
    post:
      summary: Post Notebooks Notebookid Sectiongroups
      description: Creates a new section group in a notebook.
      operationId: postNotebooksNotebookSectiongroups
      x-api-path-slug: notebooksnotebookidsectiongroups-post
      parameters:
      - in: query
        name: Content-Type
        description: 'Required: The type of content being sent'
      - in: path
        name: notebookId
        description: Specifies the notebook
      responses:
        200:
          description: OK
      tags:
      - Notebooks
      - NotebookId
      - Sectiongroups