swagger: "2.0"
x-collection-name: Azure DevTest Labs
x-complete: 1
info:
  title: DevTestLabsClient
  description: the-devtest-labs-client-
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.DevTestLab/labs/{labName}/schedules:
    get:
      summary: Schedules List
      description: List schedules in a given lab.
      operationId: Schedules_List
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devtestlablabslabnameschedules-get
      parameters:
      - in: query
        name: $expand
        description: Specify the $expand query
      - in: query
        name: $filter
        description: The filter to apply to the operation
      - in: query
        name: $orderby
        description: The ordering expression for the results, using OData notation
      - in: query
        name: $top
        description: The maximum number of resources to return from the operation
      - in: path
        name: labName
        description: The name of the lab
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Schedules
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.DevTestLab/labs/{labName}/schedules/{name}
  : get:
      summary: Schedules Get
      description: Get schedule.
      operationId: Schedules_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devtestlablabslabnameschedulesname-get
      parameters:
      - in: query
        name: $expand
        description: Specify the $expand query
      - in: path
        name: labName
        description: The name of the lab
      - in: path
        name: name
        description: The name of the schedule
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Schedules
    put:
      summary: Schedules Create Or Update
      description: Create or replace an existing schedule.
      operationId: Schedules_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devtestlablabslabnameschedulesname-put
      parameters:
      - in: path
        name: labName
        description: The name of the lab
      - in: path
        name: name
        description: The name of the schedule
      - in: query
        name: No Name
      - in: body
        name: schedule
        description: A schedule
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Schedules
    delete:
      summary: Schedules Delete
      description: Delete schedule.
      operationId: Schedules_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devtestlablabslabnameschedulesname-delete
      parameters:
      - in: path
        name: labName
        description: The name of the lab
      - in: path
        name: name
        description: The name of the schedule
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Schedules
    patch:
      summary: Schedules Update
      description: Modify properties of schedules.
      operationId: Schedules_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devtestlablabslabnameschedulesname-patch
      parameters:
      - in: path
        name: labName
        description: The name of the lab
      - in: path
        name: name
        description: The name of the schedule
      - in: query
        name: No Name
      - in: body
        name: schedule
        description: A schedule
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Schedules
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.DevTestLab/labs/{labName}/schedules/{name}/execute
  : post:
      summary: Schedules Execute
      description: Execute a schedule. This operation can take a while to complete.
      operationId: Schedules_Execute
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devtestlablabslabnameschedulesnameexecute-post
      parameters:
      - in: path
        name: labName
        description: The name of the lab
      - in: path
        name: name
        description: The name of the schedule
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Schedules
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.DevTestLab/labs/{labName}/schedules/{name}/listApplicable
  : post:
      summary: Schedules List Applicable
      description: Lists all applicable schedules
      operationId: Schedules_ListApplicable
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devtestlablabslabnameschedulesnamelistapplicable-post
      parameters:
      - in: path
        name: labName
        description: The name of the lab
      - in: path
        name: name
        description: The name of the schedule
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Schedules