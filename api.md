## Classes

<dl>
<dt><a href="#Confluence">Confluence</a></dt>
<dd></dd>
</dl>

## Members

<dl>
<dt><a href="#request">request</a></dt>
<dd><p>Node.js wrapper for Atlassian&#39;s Confluence API.
See <a href="https://developer.atlassian.com/confdev/confluence-rest-api">https://developer.atlassian.com/confdev/confluence-rest-api</a></p>
<p>Copyright (c) 2015, John Duane
Released under the MIT License</p>
</dd>
</dl>

<a name="Confluence"></a>

## Confluence
**Kind**: global class  
**this**: <code>{Confluence}</code>  

* [Confluence](#Confluence)
    * [new Confluence(config)](#new_Confluence_new)
    * [.getSpace(space, callback)](#Confluence+getSpace)
    * [.getSpaceHomePage(space, callback)](#Confluence+getSpaceHomePage)
    * [.getContentById(id, callback)](#Confluence+getContentById)
    * [.getCustomContentById(options, callback)](#Confluence+getCustomContentById)
    * [.getContentByPageTitle(space, title, callback)](#Confluence+getContentByPageTitle)
    * [.postContent(space, title, content, parentId, callback, representation)](#Confluence+postContent)
    * [.putContent(space, id, version, title, content, callback, minorEdit, representation)](#Confluence+putContent)
    * [.deleteContent(id, callback)](#Confluence+deleteContent)
    * [.getAttachments(space, id, callback)](#Confluence+getAttachments)
    * [.createAttachment(space, id, filepath, callback)](#Confluence+createAttachment)
    * [.updateAttachmentData(space, id, attachmentId, filepath, callback)](#Confluence+updateAttachmentData)
    * [.getLabels(id, callback)](#Confluence+getLabels)
    * [.postLabels(id, labels, callback)](#Confluence+postLabels)
    * [.deleteLabel(id, label, callback)](#Confluence+deleteLabel)
    * [.search(query, callback)](#Confluence+search)

<a name="new_Confluence_new"></a>

### new Confluence(config)
Construct Confluence.


| Param | Type | Description |
| --- | --- | --- |
| config | <code>Object</code> |  |
| config.username | <code>string</code> | Optional |
| config.password | <code>string</code> | Optional |
| config.pat | <code>string</code> | Optional |
| config.baseUrl | <code>string</code> |  |
| config.version | <code>number</code> | Optional |

<a name="Confluence+getSpace"></a>

### confluence.getSpace(space, callback)
Get space information.

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type |
| --- | --- |
| space | <code>string</code> | 
| callback | <code>function</code> | 

<a name="Confluence+getSpaceHomePage"></a>

### confluence.getSpaceHomePage(space, callback)
Get space home page.

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type |
| --- | --- |
| space | <code>string</code> | 
| callback | <code>function</code> | 

<a name="Confluence+getContentById"></a>

### confluence.getContentById(id, callback)
Get stored content for a specific space and page title.

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type |
| --- | --- |
| id | <code>string</code> | 
| callback | <code>function</code> | 

<a name="Confluence+getCustomContentById"></a>

### confluence.getCustomContentById(options, callback)
Get stored content for a specific page id with optional custom expanders.

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | for the custom content request |
| callback | <code>function</code> |  |

<a name="Confluence+getContentByPageTitle"></a>

### confluence.getContentByPageTitle(space, title, callback)
Get stored content for a specific space and page title.

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type |
| --- | --- |
| space | <code>string</code> | 
| title | <code>string</code> | 
| callback | <code>function</code> | 

<a name="Confluence+postContent"></a>

### confluence.postContent(space, title, content, parentId, callback, representation)
Post content to a new page.

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type | Description |
| --- | --- | --- |
| space | <code>string</code> |  |
| title | <code>string</code> |  |
| content | <code>string</code> |  |
| parentId | <code>number</code> | A null value will cause the page to be added under the space's home page |
| callback | <code>function</code> |  |
| representation | <code>string</code> | Optional |

<a name="Confluence+putContent"></a>

### confluence.putContent(space, id, version, title, content, callback, minorEdit, representation)
Put/update stored content for a page.

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type | Description |
| --- | --- | --- |
| space | <code>string</code> |  |
| id | <code>string</code> |  |
| version | <code>number</code> |  |
| title | <code>string</code> |  |
| content | <code>string</code> |  |
| callback | <code>function</code> |  |
| minorEdit | <code>boolean</code> | Optional |
| representation | <code>string</code> | Optional |

<a name="Confluence+deleteContent"></a>

### confluence.deleteContent(id, callback)
Delete a page.

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type |
| --- | --- |
| id | <code>string</code> | 
| callback | <code>function</code> | 

<a name="Confluence+getAttachments"></a>

### confluence.getAttachments(space, id, callback)
Get attachments

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type |
| --- | --- |
| space | <code>string</code> | 
| id | <code>string</code> | 
| callback | <code>function</code> | 

<a name="Confluence+createAttachment"></a>

### confluence.createAttachment(space, id, filepath, callback)
This allows you to post attachments to the pages you create.

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type | Description |
| --- | --- | --- |
| space | <code>string</code> |  |
| id | <code>string</code> |  |
| filepath | <code>string</code> | absolute path of the file you are sending |
| callback | <code>function</code> |  |

<a name="Confluence+updateAttachmentData"></a>

### confluence.updateAttachmentData(space, id, attachmentId, filepath, callback)
This allows you to update posted attachments data

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type |
| --- | --- |
| space | <code>string</code> | 
| id | <code>string</code> | 
| attachmentId | <code>string</code> | 
| filepath | <code>string</code> | 
| callback | <code>function</code> | 

<a name="Confluence+getLabels"></a>

### confluence.getLabels(id, callback)
Get labels from content

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type |
| --- | --- |
| id | <code>string</code> | 
| callback | <code>function</code> | 

<a name="Confluence+postLabels"></a>

### confluence.postLabels(id, labels, callback)
Post content labels to a existing page.

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type |
| --- | --- |
| id | <code>string</code> | 
| labels | <code>[ &#x27;Array&#x27; ].&lt;{prefix:string, name:string}&gt;</code> | 
| callback | <code>function</code> | 

<a name="Confluence+deleteLabel"></a>

### confluence.deleteLabel(id, label, callback)
Delete a label from a page.

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type |
| --- | --- |
| id | <code>string</code> | 
| label | <code>string</code> | 
| callback | <code>function</code> | 

<a name="Confluence+search"></a>

### confluence.search(query, callback)
Search by query

**Kind**: instance method of [<code>Confluence</code>](#Confluence)  

| Param | Type |
| --- | --- |
| query | <code>string</code> | 
| callback | <code>function</code> | 

<a name="request"></a>

## request
Node.js wrapper for Atlassian's Confluence API.See https://developer.atlassian.com/confdev/confluence-rest-apiCopyright (c) 2015, John DuaneReleased under the MIT License

**Kind**: global variable  
