# PZEON ADVANCE

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) `version 8.2.2`. 
`Node Version: 12.13.1`
`Angular Version: 8.2.2`

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.


## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.




## Application Level Configuration (app.config.ts)
```
  export class AppConfig {
	    public version: any = "6.4.0";
	    public headerLogo="./assets/media/logos/logo.png";
	    public isFloatingMenu: Boolean = true;
	    public landingPage = '';
	    public idpLoginURL = false;
	    public topMenuLimit = 8;
  }
  ```

## Application Menu Configuration (menu.config.ts)


###### - Tile Menu Example

```
{
	name: 'A & G Management',
	title: 'G & A  Management',
	id : "a_g_Box",
	class: 'kt-iconbox--success',
	iconUrl: './assets/media/logos/grievances-icon.png',
	disable: false,
	landingPage: '/custom/mycases'
}
```


###### - Header Menu Example
```
{
	title: 'INCIDENT LIBRARY',
	root: true,
	id: 'incidentLibrary',
	page: '',
	icon: 'fa fa-plus',
	target: "_self",
	onClick: 'createIncident',
	submenu: [
		  {
			title: 'Chart',
			bullet: 'dot',
			icon: 'fa fa-plus',
			page: '/custom/chart',
			submenu: [{
				title: 'Pie',
				bullet: 'dot',
				icon: 'fa fa-plus',
				page: '/custom/pie'
			   }]
		  }
	],
	notification: {
	    badge: {
		value: 0,
		class: 'info'
	    },
	    scheduler: {
		time: 300000,
		status: true,
		method: 'countExpediteCaseNotification'
	    }
       }
  }
  ```
## Bundle Configuration (bundle.config.ts)

        {
        	"id": 6100,
        	"name": "Case Details",
        	"owner": "Mohar",
        	"showCustomView": true,
        	"isPublicThread": true,
        	"hasDefaultTemplate": true,
        	"showNavigationMenu": true,
        	"defaultTemplate": {
        		"id": "120000",
        		"name": "IncidentDetails"
        	},
        	"templateSelectionOption": "true",
        	"description": "",
        	"desktopView": {
        		"showPDFExport": true,
        		"showPreview": true,
        		"dashboardGroup": [],
        		"dashboards": [],
        		"navConfig": {
        			"newthreads": "Incident Details",
        			"inbox": "Incident Details",
        			"view": "Message"
        		},
        		"stepperConfig": {
        			"displayHtml": "finalStepDisplayHtml"
        		},
        		"uiConfig": {
        			"visibility": {
        				"newThread": true,
        				"inbox": false
        			},
        			"displayName": {
        				"newThread": "Incident Details",
        				"inbox": "Incident Details"
        			},
        			"iconCls": {},
        			"css": {},
        			"defaultNavigationSelection": "inbox"
        		},
        		"newThreadUIConfig": {
        			"visibility": {},
        			"displayName": {}
        		},
        		"myThreadUIConfig": {
        			"displayHtml": "getThreadTitleInfo"
        		},
        		"inboxUIConfig": {
        			"isGridView": true,
        			"gridViewConfig": [{
        					"name": "member_id",
        					"label": "Member ID",
        					"width": "100px"
        				}, {
        					"name": "incidentId",
        					"label": "Case ID",
        					"width": "150px"
        				},
        				{
        					"name": "caseShortDescription",
        					"label": "Case Short Description",
        					"width": "200px"
        				},
        				{
        					"name": "assignmentStatus",
        					"label": "Assignment Status",
        					"width": "200px"
        				},
        				{
        					"name": "createdAt",
        					"label": "Created At",
        					"width": "100px"
        				}
        			],
        			"gridViewActionButtons": [{
        				"name": "grievance",
        				"text": "Grievance",
        				"icon": "fa fa-file",
        				"click": "onGrievanceClick"
        			}],
        			"showRmvBtn": true,
        			"showEditBtn": false,
        			"showAddBtn": true,
        			"showExpandBtn": true,
        			"showVersionBtn": false,
        			"showMsgIcon": true,
        			"showMsgDetailsInHTML": false,
        			"msgIcon": "fa fa-file-text-o",
        			"showRemark": false,
        			"displayHtml": "incidentDetailsDisplayHtml",
        			"kpiTilesList": [{
        					"customQuery": {
        						"method": "loadKPIDataList",
        						"param": "All Incident"
        					},
        					"displayText": "All Incident(S)",
        					"name": "allIncidents",
        					"cls": "kt-font-warning",
        					"id": "allIncidents",
        					"alertBoxCls": "box-3",
        					"icon": "<i class='fa fa-calendar'></i>",
        					"countQry": {
        						"method": "loadKPICount",
        						"param": "All Incident"
        					}
        				},
        				{
        					"customQuery": {
        						"method": "loadKPIDataList",
        						"param": "Action Taken"
        					},
        					"displayText": "ACTION TAKEN",
        					"name": "actionTakenIncidents",
        					"cls": "kt-font-danger",
        					"id": "actionTakenIncidents",
        					"alertBoxCls": "box-4",
        					"icon": "<i class='fa fa-calendar'></i>",
        					"countQry": {
        						"method": "loadKPICount",
        						"param": "Action Taken"
        					}
        				},
        				{
        					"customQuery": {
        						"method": "loadKPIDataList",
        						"param": "Action Not Taken"
        					},
        					"displayText": "ACTION NOT TAKEN",
        					"name": "actionNotTakenIncidents",
        					"cls": "kt-font-success",
        					"id": "actionNotTakenIncidents",
        					"alertBoxCls": "box-5",
        					"icon": "<i class='fa fa-calendar'></i>",
        					"countQry": {
        						"method": "loadKPICount",
        						"param": "Action Not Taken"
        					}
        				},
        				{
        					"customQuery": {
        						"method": "loadKPIDataList",
        						"param": "My Incident"
        					},
        					"displayText": "MY INCIDENT(S)",
        					"name": "myIncidents",
        					"id": "myIncidents",
        					"cls": "kt-font-brand",
        					"alertBoxCls": "box-6",
        					"icon": "<i class='fa fa-calendar'></i>",
        					"countQry": {
        						"method": "loadKPICount",
        						"param": "My Incident"
        					}
        				}
        			],
        			"defaultQuery": {
        				"bundleId": 6100,
        				"isTrash": false
        			},
        			"advanceSearchQuery": {
        				"bundleId": 6100,
        				"isTrash": false
        			},
        			"sortConfig": [{
        				"createdAt": -1
        			}],
        			"sortConfigList": [{
        					"incidentId": "Incident Id"
        				},
        				{
        					"member_id": "Member Id"
        				}
        			],
        			"searchParams": [{
        					"name": "recentData.member_id",
        					"class": "col-md-12",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"disabled": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.assignmentStatus",
        					"class": "col-md-12",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"disabled": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.incidentId",
        					"class": "col-md-12",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.member_firstname",
        					"class": "col-md-12",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.member_lastname",
        					"class": "col-md-12",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.memberTelephoneNumber",
        					"class": "col-md-12",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.memberDob",
        					"class": "col-md-12",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.incidentForm",
        					"class": "col-md-12",
        					"operator": "$eq"
        				},
        				{
        					"name": "recentData.incidentStatus",
        					"class": "col-md-12",
        					"operator": "$eq"
        				},
        				{
        					"name": "recentData.caseType",
        					"class": "col-md-12",
        					"operator": "$eq"
        				},
        				{
        					"name": "recentData.receivedDate",
        					"class": "col-md-12",
        					"operator": "$eq"
        				},
        				{
        					"name": "recentData.memberId",
        					"class": "col-md-12",
        					"operator": "$eq"
        				}
        			],
        			"visibleItemsCount": 10,
        			"basicSearchParams": [{
        				"name": "recentData.project"
        			}],
        			"displayFields": [],
        			"hasToolBox": true,
        			"toolBoxItems": [

        				{
        					"widget": "button",
        					"id": "a_g_actionBtn",
        					"name": "a_g_actionBtn",
        					"text": "Attach to",
        					"css": "btn btn-primary btn-squared",
        					"iconClass": "fa fa-paperclip",
        					"listeners": [{
        						"event": "click",
        						"enabled": true,
        						"script": {
        							"methodName": "onAttachClick",
        							"param": "thread"
        						}
        					}]
        				},
        				{
        					"widget": "button",
        					"id": "a_g_actionBtn",
        					"name": "a_g_actionBtn",
        					"text": "Options",
        					"css": "btn btn-primary btn-squared",
        					"iconClass": "fa fa-cog",
        					"listeners": [{
        						"event": "click",
        						"enabled": true,
        						"script": {
        							"methodName": "createAGActionInfo",
        							"param": "thread"
        						}
        					}]
        				}
        			],
        			"preScript": "incidentDetailsPreScript",
        			"postScript": "incidentDetailsPostScript",
        			"onBundleLoad": "incidentDetailBundleLoad"
        		}

        	}
        }
	
## Box Configuration (box.config.ts)

        {
        	"id": 161,
        	"name": "Grievances",
        	"owner": "Mohar",
        	"createdAt": "17 Dec 2018",
        	"description": "Description goes here...",
        	"showNavigationMenu": true,
        	"showAddBtn": false,
        	"showEditBtn": true,
        	"showRmvBtn": true,
        	"masterBundle": 6101,
        	"slaveBundles": [
        		6123,
        		6121,
        		6104,
        		6124,
        		6105,
        		6125,
        		6122,
        		6106

        	],
        	"replicationConfig": {
        		"6101.recentData.assignedTo": "6100.recentData.assignedTo"
        	},
        	"defaultTemplate": {
        		"id": "120001",
        		"name": "GrievanceIntakeSummary"
        	},
        	"dataAttributes": {},
        	"desktopView": {
        		"showPDFExport": true,
        		"showPreview": true,
        		"fullBoxUIConfig": {
        			"displayHtml": "getBoxTitleInfo"
        		},
        		"boxUIConfig": {
        			"showAddBtn": false,
        			"showMsgIcon": true,
        			"msgIcon": "fa fa-file-text-o",
        			"showVersionBtn": false,
        			"displayHtml": "grievanceDisplayHtml",
        			"hasToolBox": false,
        			"toolBoxItems": [],
        			"sortConfig": [{
        				"createdAt": -1
        			}],
        			"sortConfigList": [{
        					"incidentId": "Incident Id"
        				},
        				{
        					"caseType": "Case Type"
        				},
        				{
        					"regulatoryDuedateWizardISODate": "Due Date"
        				}
        			],
        			"globalTextSearchEnable": true,
        			"searchParams": [{
        					"name": "recentData.member_id",
        					"class": "col-md-6",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"disabled": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.incidentId",
        					"class": "col-md-6",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"disabled": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.grievanceId",
        					"class": "col-md-6",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"disabled": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.caseType",
        					"class": "col-md-6",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"disabled": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.caseStatus",
        					"class": "col-md-6",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"disabled": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.isThisvalidComplaint",
        					"class": "col-md-6",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"disabled": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.qualityOfCareIssuesRaised",
        					"class": "col-md-6 searchFilterRadioGroup",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"disabled": false,
        						"value": ""
        					}
        				},
        				{
        					"name": "recentData.qualityOfServiceIssuesRaised",
        					"class": "col-md-6 searchFilterRadioGroup",
        					"operator": "$eq",
        					"propConfigs": {
        						"hidden": false,
        						"disabled": false,
        						"value": ""
        					}
        				}

        			],
        			"visibleItemsCount": 8,
        			"projection": {}
        		}
        	},
        	"$$hashKey": "object:130"
        }
	
## Widget Configuration

#### Bundle Filter Widget
```
{
	"name": "incidentClosedBy",
	"singleSelect": true,
	"text": "Incident Closed By",
	"HeaderText": "Incident Closed By",
	"widget": "bundleFilter",
	"oneLiner": true,
	"disabled": false,
	"hidden": false,
	"mandatory": false,
	"tabIndex": 1,
	"listeners": {
		"change": {
			"methodName": "update",
			"param": "value"
		}
	},
	"bundleInfo": {
		"minCharacterForLikeSearch": 3,
		"bundleId": 7100,
		"key": "recentData.userFullName",
		"value": "recentData.userID",
		"defaultLoadQuery": {
			"recentData#member_id": ""
		},
		"defaultQuery": {
			"recentData#member_id": ""
		},
		"displayList": [{
				"label": "Full Name",
				"key": "userFullName",
				"value": "recentData.userFullName"
			},
			{
				"label": "User Id",
				"key": "userID",
				"value": "recentData.userID"
			},
			{
				"label": "EmailId",
				"key": "userEmailId",
				"value": "recentData.userEmailId"
			}
		],
		"filters": [{
				"label": "Member ID",
				"key": "recentData.member_id",
				"value": "recentData.member_id",
				"widget": "textfield",
				"likeSearch": true,
				"linkToparent": false
			},
			{
				"label": "Member First Name",
				"key": "recentData.memberFirstName",
				"value": "recentData.memberFirstName",
				"widget": "textfield",
				"likeSearch": true,
				"linkToparent": false
			},
			{
				"label": "Date of Birth",
				"key": "recentData.memberDob",
				"value": "recentData.memberDob",
				"type": "date",
				"widget": "datefield",
				"likeSearch": true,
				"linkToparent": false
			}
		]
	}
}
```
| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "incidentClosedBy" |
| singleSelect  | Boolean  | Allow user select multiple items | true or false |
| text  | String  | Label for the widget | "Incident Closed By" |
| HeaderText  | String  | Title of the bundle filter modal | "Incident Closed By" |
| widget  | String  | Name of the widget |  "bundleFilter" |
| oneLiner  | Boolean  | Oneliner view status | true or false |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| mandatory  | Boolean  | Mandatory status of the widget | true or false |
| tabIndex  | Number  | Tab index for the widget | true or false |
| listeners  | Object  | Contain listers information for the widget | true or false |
| bundleInfo.minCharacterForLikeSearch  | Number  | Minimum character for search | 3 |
| bundleInfo.bundleId  | Number  | Bundle Id for Search | 7100 |
| bundleInfo.key  | String  | Key for Search | "recentData.userFullName" |
| bundleInfo.value  | String  | Value for search | "recentData.userID" |
| bundleInfo.defaultLoadQuery  | Object  | Execute a query when bundle filter loads | "defaultLoadQuery": "{"recentData#member_id" : "" }", |
| bundleInfo.defaultQuery  | Object  | Execute a query on search | "defaultQuery": "{"recentData#member_id" : "" }", |
| bundleInfo.defaultSortQuery  | Object  | Execute a query on search used for sorting operation | "defaultSortQuery": "{"recentData#member_id" : "" }", |
| bundleInfo.displayList  | Array of Object  | Contain list of object having the display information on search | |
| bundleInfo.filters  | Array of Object  | Contain list of object having the filter information of bundle filter | |

