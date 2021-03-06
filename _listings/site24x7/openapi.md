swagger: "2.0"
x-collection-name: Site24x7
x-complete: 1
info:
  title: User Group API
  description: the-user-group-api-
  version: 1.0.0
host: www.site24x7.com.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /scheduled_reports:
    post:
      summary: Schedule a Report
      description: Schedule a report to be received on a specific day and time.
      operationId: schedule-a-report
      x-api-path-slug: scheduled-reports-post
      parameters:
      - in: path
        name: "display_name\n        \n        \n            required\n            Display
          name for the Report.\n        \n    \n    \n        \n        report_type\n
          \       \n        \n            required\n            Type of report to
          be Scheduled.Report Constants"
      responses:
        200:
          description: OK
      tags:
      - Scheduled Reports
    get:
      summary: List Scheduled Reports
      description: List of all Scheduled Reports.
      operationId: list-scheduled-reports
      x-api-path-slug: scheduled-reports-get
      parameters:
      - in: path
        name: "sla_id\n        \n        \n            string\n            Unique
          ID generated by the server. This can be used as an identifier.\n        \n
          \               \n    \n        \n        display_name\n        \n        \n
          \           string\n            Display name f"
      responses:
        200:
          description: OK
      tags:
      - Scheduled Reports
  /scheduled_reports/{report_id}:
    put:
      summary: Update Scheduled Report
      description: Update the configuration of an existing Scheduled Report.
      operationId: update-scheduled-report
      x-api-path-slug: scheduled-reportsreport-id-put
      parameters:
      - in: path
        name: "display_name\n        \n        \n            required\n            Display
          name for the Report.\n        \n    \n    \n        \n        report_type\n
          \       \n        \n            required\n            Type of report to
          be Scheduled.Report Constants"
      responses:
        200:
          description: OK
      tags:
      - Scheduled Reports