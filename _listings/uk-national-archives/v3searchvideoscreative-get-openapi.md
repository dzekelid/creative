---
swagger: "2.0"
x-collection-name: UK National Archives
x-complete: 0
info:
  title: Getty Images Search API Get Search Veos Creative
  description: Search for creative videos.
  version: "3.0"
host: api.gettyimages.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/search/images/creative:
    get:
      summary: Get Search Images Creative
      description: Search for creative images only.
      operationId: getV3SearchImagesCreative
      x-api-path-slug: v3searchimagescreative-get
      parameters:
      - in: header
        name: Accept-Language
        description: Specifies the language of result values
      - in: query
        name: age_of_people
        description: Filter based on the age of individuals in an image
      - in: query
        name: artists
        description: Search for images by specific artists (free-text, comma-separated
          list of artists)
      - in: header
        name: Authorization
        description: Provide access token in the format of Bearer {token}
      - in: query
        name: collections_filter_type
        description: Use to include or exclude collections from search
      - in: query
        name: collection_codes
        description: Filter by collection codes (comma-separated list)
      - in: query
        name: color
        description: Filter based on predominant color in an image
      - in: query
        name: compositions
        description: Filter based on image composition
      - in: query
        name: embed_content_only
        description: Restrict search results to embeddable images
      - in: query
        name: ethnicity
        description: Filter search results based on the ethnicity of individuals in
          an image
      - in: query
        name: exclude_nudity
        description: Excludes images containing nudity
      - in: query
        name: fields
        description: Specifies fields to return
      - in: query
        name: file_types
        description: Return only images having a specific file type
      - in: query
        name: graphical_styles
        description: Filter based on graphical style of the image
      - in: query
        name: keyword_ids
        description: Return only images tagged with specific keyword(s)
      - in: query
        name: license_models
        description: Specifies the image licensing model(s)
      - in: query
        name: minimum_size
        description: Filter based on minimum size requested
      - in: query
        name: number_of_people
        description: Filter based on the number of people in the image
      - in: query
        name: orientations
        description: Return only images with selected aspect ratios
      - in: query
        name: page
        description: Request results starting at a page number (default is 1)
      - in: query
        name: page_size
        description: Request number of images to return in each page
      - in: query
        name: phrase
        description: Search images using a search phrase
      - in: query
        name: prestige_content_only
        description: Restrict search results to prestige images
      - in: query
        name: product_types
        description: Filter images to those having product types from the selected
          list
      - in: query
        name: sort_order
        description: Select sort order of results
      responses:
        200:
          description: OK
      tags:
      - Search
      - Images
      - Creative
  /v3/search/videos/creative:
    get:
      summary: Get Search Veos Creative
      description: Search for creative videos.
      operationId: getV3SearchVeosCreative
      x-api-path-slug: v3searchvideoscreative-get
      parameters:
      - in: header
        name: Accept-Language
        description: Specifies the language of result values
      - in: query
        name: age_of_people
        description: Provides filtering according to the age of individuals in a video
      - in: header
        name: Authorization
        description: Provide access token in the format of Bearer {token}
      - in: query
        name: collections_filter_type
        description: Provides searching based on specified collection(s)
      - in: query
        name: collection_codes
        description: Provides filtering by collection code
      - in: query
        name: exclude_nudity
        description: Excludes images containing nudity
      - in: query
        name: fields
        description: Specifies fields to return
      - in: query
        name: format_available
        description: Filters according to the digital video format available on a
          film asset
      - in: query
        name: keyword_ids
        description: Return only images tagged with specific keyword(s)
      - in: query
        name: license_models
        description: Specifies the video licensing model(s)
      - in: query
        name: page
        description: Identifies page to return
      - in: query
        name: page_size
        description: Specifies page size
      - in: query
        name: phrase
        description: Free-text search query
      - in: query
        name: product_types
        description: Allows filtering by a list of product types
      - in: query
        name: sort_order
        description: Allows sorting of results
      responses:
        200:
          description: OK
      tags:
      - Search
      - Veos
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