{
  "info": {
    "name": "One Note Get Sections",
    "_postman_id": "443d2866-eef0-4372-8868-1f6e42afa305",
    "description": "Returns a collection of sections.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Sections",
      "item": [
        {
          "id": "07608e39-f43e-4277-88e8-266d96eb8e48",
          "name": "getSections",
          "request": {
            "url": "http://www.onenote.com/api/v1.0/me/notes/sections/?count=%7B%7D&expand=%7B%7D&filter=%7B%7D&orderby=%7B%7D&select=%7B%7D&skip=%7B%7D&top=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a collection of sections."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fc53b0ce-57c7-4eba-a84a-b9fc8daa20dd"
            }
          ]
        }
      ]
    }
  ]
}