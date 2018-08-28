---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Sections API Delete a section
  description: Delete a section.
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
  /courses/{course_id}/sections:
    get:
      summary: List course sections
      description: List course sections.
      operationId: list-course-sections
      x-api-path-slug: coursescourse-idsections-get
      parameters:
      - in: query
        name: include[]
        description: 'u201cstudentsu201d: Associations to include with the group'
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Sections
    post:
      summary: Create course section
      description: Create course section.
      operationId: create-course-section
      x-api-path-slug: coursescourse-idsections-post
      parameters:
      - in: query
        name: course_section[end_at]
        description: Section end date in ISO8601 format
      - in: query
        name: course_section[name]
        description: The name of the section
      - in: query
        name: course_section[restrict_enrollments_to_section_dates]
        description: Set to true to restrict user enrollments to the start and end
          dates of thensection
      - in: query
        name: course_section[sis_section_id]
        description: The sis ID of the section
      - in: query
        name: course_section[start_at]
        description: Section start date in ISO8601 format, e
      - in: query
        name: enable_sis_reactivation
        description: When true, will first try to re-activate a deleted section with
          matchingnsis_section_id if possible
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Sections
  /courses/{course_id}/sections/id:
    get:
      summary: Get section information
      description: Get section information.
      operationId: get-section-information
      x-api-path-slug: coursescourse-idsectionsid-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Sections
      - Id
  /sections/{course_section_id}/assignments/assignment_id/override:
    get:
      summary: Redirect to the assignment override for a section
      description: Redirect to the assignment override for a section.
      operationId: redirect-to-the-assignment-override-for-a-section
      x-api-path-slug: sectionscourse-section-idassignmentsassignment-idoverride-get
      responses:
        200:
          description: OK
      tags:
      - Sections
      - Course
      - Section
      - Id
      - Assignments
      - Assignment
      - Id
      - Override
  /sections/{id}:
    delete:
      summary: Delete a section
      description: Delete a section.
      operationId: delete-a-section
      x-api-path-slug: sectionsid-delete
      responses:
        200:
          description: OK
      tags:
      - Sections
      - Id
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