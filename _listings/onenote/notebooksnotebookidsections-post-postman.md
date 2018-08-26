{
  "info": {
    "name": "One Note Post Notebooks Notebookid Sections",
    "_postman_id": "014b0677-fb47-484d-8dc1-1fffb8640fd3",
    "description": "Creates a new section in a specific notebook.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Notebooks",
      "item": [
        {
          "id": "491cf2bf-37a6-44d1-9dfa-6354c9e8a898",
          "name": "getNotebooksNotebookSections",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.onenote.com",
              "path": [
                "api",
                "v1.0",
                "me",
                "notes",
                "notebooks/:notebookId/sections"
              ],
              "query": [
                {
                  "key": "count",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "orderby",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "select",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "skip",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "top",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "notebookId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a collection of sections within a specific notebook."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8a72feae-9383-480f-a8d5-7823623cf751"
            }
          ]
        },
        {
          "id": "45aa3d3a-4a83-41c5-b412-8c095d415a15",
          "name": "postNotebooksNotebookSections",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.onenote.com",
              "path": [
                "api",
                "v1.0",
                "me",
                "notes",
                "notebooks/:notebookId/sections"
              ],
              "variable": [
                {
                  "id": "notebookId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "Required: indicates type of content being sent",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new section in a specific notebook."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "144ae2b1-27f9-4515-b5f0-124f5589d074"
            }
          ]
        }
      ]
    }
  ]
}