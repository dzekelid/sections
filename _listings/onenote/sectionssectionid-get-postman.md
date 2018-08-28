{
  "info": {
    "name": "One Note Get Sections Sectionid",
    "_postman_id": "bdd167b4-f154-489a-9b19-6d6b13a9a5f2",
    "description": "Returns a specific section.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Sections",
      "item": [
        {
          "id": "1ea073e6-b7e1-4116-a24f-92c1b049ff22",
          "name": "getSectionsSection",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.onenote.com",
              "path": [
                "api",
                "v1.0",
                "me",
                "notes",
                "sections/:sectionId"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "select",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "sectionId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a specific section."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f8fd63df-3847-4f38-98b4-d3f42a2343fc"
            }
          ]
        }
      ]
    }
  ]
}