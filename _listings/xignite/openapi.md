swagger: "2.0"
x-collection-name: Xignite
x-complete: 1
info:
  title: Xignite VWAP
  description: provides-delayed-and-historical-volumeweightedaverage-price-vwap-information-
  version: 1.0.0
host: www.xignite.com
basePath: xVWAP.json/XigniteVWAP
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /GetMasterBySector:
    get:
      summary: Get Master By Sector
      description: Old version of the service. Customers should use GetMasterByGlobalSector
      operationId: GetMasterBySector
      x-api-path-slug: getmasterbysector-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Master
      - Sector
  /GetMasterByGlobalSector:
    get:
      summary: Get Master By Global Sector
      description: Get master records by sector.
      operationId: GetMasterByGlobalSector
      x-api-path-slug: getmasterbyglobalsector-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Master
      - Global
      - Sector
  /GetTopMarketHeadlinesBySector:
    get:
      summary: Get Top Market Headlines By Sector
      description: Returns the most recent specified number of market headlines associated
        with a specified sector.
      operationId: GetTopMarketHeadlinesBySector
      x-api-path-slug: gettopmarketheadlinesbysector-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Top
      - Market
      - Headlines
      - Sector
  /GetTodaysMarketHeadlinesBySector:
    get:
      summary: Get Todays Market Headlines By Sector
      description: Returns all market headlines that were published today for a specified
        sector.
      operationId: GetTodaysMarketHeadlinesBySector
      x-api-path-slug: gettodaysmarketheadlinesbysector-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Todays
      - Market
      - Headlines
      - Sector
  /GetHistoricalMarketHeadlinesBySector:
    get:
      summary: Get Historical Market Headlines By Sector
      description: Returns all market headlines that were published in a specified
        time frame for a specified sector.
      operationId: GetHistoricalMarketHeadlinesBySector
      x-api-path-slug: gethistoricalmarketheadlinesbysector-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Historical
      - Market
      - Headlines
      - Sector