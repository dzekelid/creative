---
swagger: "2.0"
x-collection-name: Google Doubleclick
x-complete: 0
info:
  title: Google Doubleclick API Insert Creative
  version: 1.0.0
  description: Inserts a new creative.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /creatives:
    get:
      summary: Get Creatives
      description: Retrieves a list of the authenticated user's active creatives.
        A creative will be available 30-40 minutes after submission.
      operationId: adexchangebuyer.creatives.list
      x-api-path-slug: creatives-get
      parameters:
      - in: query
        name: accountId
        description: When specified, only creatives for the given account ids are
          returned
      - in: query
        name: buyerCreativeId
        description: When specified, only creatives for the given buyer creative ids
          are returned
      - in: query
        name: dealsStatusFilter
        description: When specified, only creatives having the given deals status
          are returned
      - in: query
        name: maxResults
        description: Maximum number of entries returned on one result page
      - in: query
        name: openAuctionStatusFilter
        description: When specified, only creatives having the given open auction
          status are returned
      - in: query
        name: pageToken
        description: A continuation token, used to page through ad clients
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Creative
    post:
      summary: Submit Creative
      description: Submit a new creative.
      operationId: adexchangebuyer.creatives.insert
      x-api-path-slug: creatives-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Creative
  /creatives/{accountId}/{buyerCreativeId}:
    get:
      summary: Get Creative Status
      description: Gets the status for a single creative. A creative will be available
        30-40 minutes after submission.
      operationId: adexchangebuyer.creatives.get
      x-api-path-slug: creativesaccountidbuyercreativeid-get
      parameters:
      - in: path
        name: accountId
        description: The id for the account that will serve this creative
      - in: path
        name: buyerCreativeId
        description: The buyer-specific id for this creative
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Creative
  /userprofiles/{profileId}/creatives:
    get:
      summary: Get Creatives
      description: Retrieves a list of creatives, possibly filtered. This method supports
        paging.
      operationId: dfareporting.creatives.list
      x-api-path-slug: userprofilesprofileidcreatives-get
      parameters:
      - in: query
        name: active
        description: Select only active creatives
      - in: query
        name: advertiserId
        description: Select only creatives with this advertiser ID
      - in: query
        name: archived
        description: Select only archived creatives
      - in: query
        name: campaignId
        description: Select only creatives with this campaign ID
      - in: query
        name: companionCreativeIds
        description: Select only in-stream video creatives with these companion IDs
      - in: query
        name: creativeFieldIds
        description: Select only creatives with these creative field IDs
      - in: query
        name: ids
        description: Select only creatives with these IDs
      - in: query
        name: maxResults
        description: Maximum number of results to return
      - in: query
        name: pageToken
        description: Value of the nextPageToken from the previous result page
      - in: path
        name: profileId
        description: User profile ID associated with this request
      - in: query
        name: renderingIds
        description: Select only creatives with these rendering IDs
      - in: query
        name: searchString
        description: Allows searching for objects by name or ID
      - in: query
        name: sizeIds
        description: Select only creatives with these size IDs
      - in: query
        name: sortField
        description: Field by which to sort the list
      - in: query
        name: sortOrder
        description: Order of sorted results, default is ASCENDING
      - in: query
        name: studioCreativeId
        description: Select only creatives corresponding to this Studio creative ID
      - in: query
        name: types
        description: Select only creatives with these creative types
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Creative
    patch:
      summary: Update Creative
      description: Updates an existing creative. This method supports patch semantics.
      operationId: dfareporting.creatives.patch
      x-api-path-slug: userprofilesprofileidcreatives-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: id
        description: Creative ID
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Creative
    post:
      summary: Insert Creative
      description: Inserts a new creative.
      operationId: dfareporting.creatives.insert
      x-api-path-slug: userprofilesprofileidcreatives-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: profileId
        description: User profile ID associated with this request
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Creative
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