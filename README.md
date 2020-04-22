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
			"methodName": "update"
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
| listeners  | Object  | Contain listers information for the widget | "change": {"methodName": "update"} |
| bundleInfo.minCharacterForLikeSearch  | Number  | Minimum character for search | 3 |
| bundleInfo.bundleId  | Number  | Bundle Id for Search | 7100 |
| bundleInfo.key  | String  | Key for Search | "recentData.userFullName" |
| bundleInfo.value  | String  | Value for search | "recentData.userID" |
| bundleInfo.defaultLoadQuery  | Object  | Execute a query when bundle filter loads | "defaultLoadQuery": "{"recentData#member_id" : "" }", |
| bundleInfo.defaultQuery  | Object  | Execute a query on search | "defaultQuery": "{"recentData#member_id" : "" }", |
| bundleInfo.defaultSortQuery  | Object  | Execute a query on search used for sorting operation | "defaultSortQuery": "{"recentData#member_id" : "" }", |
| bundleInfo.displayList  | Array of Object  | Contain list of object having the display information on search | |
| bundleInfo.filters  | Array of Object  | Contain list of object having the filter information of bundle filter | |



#### Comment widget

     {
     	"name": "nonMedicalReviewerComment",
     	"text": "Reviewer's Comment",
     	"widget": "comment",
     	"emptyText": "Type your comment here...",
     	"emptyCommentText": "No comments added yet",
     	"commentTimeFormat": "MM-DD-YYYY hh:mm:ss",
     	"commentOrder": "desc",
     	"canUserDelete": true,
     	"canAdminDelete": false,
     	"showCount": true,
     	"listeners": {
     		"change": {
     			"methodName": "update"
     		}
     	}
     }

| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "caseType" |
| text  | String  | Label for the widget | "Case Type" |
| widget  | String  | Name of the widget |  "comment" |
| oneLiner  | Boolean  | Oneliner view status | true or false |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| mandatory  | Boolean  | Mandatory status of the widget | true or false |
| tabIndex  | Number  | Tab index for the widget | true or false |
| emptyText  | String  | Text for placeholder | "Type your comment here..." |
| emptyCommentText  | String  | Display this text if there is no comment | "No comments added yet" |
| commentTimeFormat  | String  | Timeformat to display in comment widget | "MM-DD-YYYY hh:mm:ss" |
| canUserDelete  | Boolean  | Giving permission to user for delete comment | true or false |
| canAdminDelete  | Boolean  | Giving permission to admin for delete comment | true or false |
| showCount  | true  | Show status of the count value in comment widget | true or false |
| listeners  | Object  | Contain listers information for the widget | "change": {"methodName": "update"} |

#### Combo widget

##### Normal Combo
```
{
	"name": "caseType",
	"text": "Case Type",
	"description": "Case Type",
	"oneLiner": true,
	"type": "string",
	"tabIndex": 1,
	"widget": "combo",
	"listeners": {
    	"change": {
     		"methodName": "caseTypeChange"
     	}
    },
	"properties": {
		"datasource": [
			"High",
			"Medium High",
			"Medium",
			"Low"
		],
		"multiselect": false
	},
	"mandatory": true
}
```

##### Hierarchical Combo

###### Parent Combo
```
{
  "name": "grievanceCategory",
  "text": "Grievance Category",
  "dataIndex": "grievanceCategory",
  "renderer": "",
  "width": "100px",
  "description": "Grievance Category",
  "securityContext": false,
  "type": "string",
  "tabIndex": 1,
  "tooltip": {
    "enabled": false,
    "format": null
  },
  "mandatory": false,
  "hidden": true,
  "ownerEditable": false,
  "widget": "combo",
  "selectAllOption": true,
  "selectAllOptionText": "All",
  "properties": {
    "datasource": [
      "ACCESS AND AVAILABILITY",
      "MARKETING",
      "ENROLLMENT/DISENROLLMENT",
      "QUALITY OF CARE",
      "QUALITY OF SERVICE",
      "POTENTIAL FRAUD/ABUSE",
      "BILLING/FINANCIAL DISPUTE",
      "CONFIDENTIALITY/PRIVACY",
      "BENEFIT PACKAGE",
      "APPEALS",
      "GRIEVANCES",
      "CMS ISSUES"
    ],
    "grievanceSubcategoryOptions": [
      {
        "masterValue": "ACCESS AND AVAILABILITY",
        "options": [
          "DENTAL",
          "HOSPITAL",
          "MAIL ORDER REFILLS",
          "PCP",
          "SPECIALIST",
          "PHARMACY",
          "PLAN",
          "DISCRIMINATION",
          "ANCILLARIES",
          "OTHER"
        ]
      },
      {
        "masterValue": "MARKETING",
        "options": [
          "AGENT ALLEGATION",
          "MARKETING MATERIALS",
          "OTHER"
        ]
      },
      {
        "masterValue": "ENROLLMENT/DISENROLLMENT",
        "options": [
          "ENROLLMENT/DISENROLLMENT DATE",
          "ENROLLMENT MATERIALS",
          "INVOLUNTARY ENROLLMENT/DISENROLLMENT",
          "OTHER"
        ]
      },
      {
        "masterValue": "QUALITY OF CARE",
        "options": [
          "DENTAL",
          "HOSPITAL",
          "PCP",
          "SPECIALIST",
          "PHARMACY",
          "ANCILLARIES",
          "OTHER"
        ]
      },
      {
        "masterValue": "QUALITY OF SERVICE",
        "options": [
          "NOT SATISFIED WITH PLAN SERVICES",
          "NOT SATISFIED WITH PROVIDER SERVICES",
          "CARE MANAGEMENT PROGRAMS",
          "DISCRIMINATION",
          "SALES INTEGRITY",
          "OTHER"
        ]
      },
      {
        "masterValue": "POTENTIAL FRAUD/ABUSE",
        "options": [
          "SERVICES WERE NEVER RENDERED",
          "MEDICATION NOT RECEIVED",
          "OTHER"
        ]
      },
      {
        "masterValue": "BILLING/FINANCIAL DISPUTE",
        "options": [
          "BALANCE BILLING",
          "PROVIDER CLAIM ISSUES",
          "OTHER"
        ]
      },
      {
        "masterValue": "BENEFIT PACKAGE",
        "options": [
          "CO-PAYMENT ISSUES",
          "BENEFITS AVAILABLE IN PLAN",
          "VAIS",
          "OTHER"
        ]
      },
      {
        "masterValue": "CONFIDENTIALITY/PRIVACY",
        "options": [
          "HIPAA VIOLATION/PRIVACY BREACH"
        ]
      },
      {
        "masterValue": "APPEALS",
        "options": [
          "PLAN RESPONSE UNSATISFACTORY/UNTIMELY",
          "PLAN DOES NOT PROVIDE APPROPRIATE APPEALS PROCESS",
          "OTHER",
          "DECLINED EXPEDITED TIMEFRAME (ETD)",
          "DISSATISFIED WITH TIMEFRAME EXTENSION (PTE)"
        ]
      },
      {
        "masterValue": "GRIEVANCES",
        "options": [
          "PLAN RESPONSE UNSATISFACTORY/UNTIMELY",
          "PLAN DOES NOT PROVIDE APPROPIATE GRIEVANCE PROCESS",
          "OTHER"
        ]
      },
      {
        "masterValue": "CMS ISSUES",
        "options": [
          "OTHER"
        ]
      }
    ],
    "partCCMSCategoryOptions": [
      {
        "masterValue": "ACCESS AND AVAILABILITY",
        "options": [
          "ACCESS"
        ]
      },
      {
        "masterValue": "CMS ISSUES",
        "options": [
          "GRIEVANCES RELATED TO CMS ISSUES"
        ]
      },
      {
        "masterValue": "MARKETING",
        "options": [
          "MARKETING"
        ]
      },
      {
        "masterValue": "ENROLLMENT/DISENROLLMENT",
        "options": [
          "ENROLLMENT/DISENROLLMENT"
        ]
      },
      {
        "masterValue": "QUALITY OF CARE",
        "options": [
          "QUALITY OF CARE"
        ]
      },
      {
        "masterValue": "QUALITY OF SERVICE",
        "options": [
          "CUSTOMER SERVICE"
        ]
      },
      {
        "masterValue": "POTENTIAL FRAUD/ABUSE",
        "options": [
          "OTHER"
        ]
      },
      {
        "masterValue": "BILLING/FINANCIAL DISPUTE",
        "options": [
          "OTHER"
        ]
      },
      {
        "masterValue": "BENEFIT PACKAGE",
        "options": [
          "BENEFIT PACKAGE"
        ]
      },
      {
        "masterValue": "CONFIDENTIALITY/PRIVACY",
        "options": [
          "OTHER"
        ]
      },
      {
        "masterValue": "APPEALS",
        "options": [
          "ORGANIZATION DETERMINATION AND RECONSIDERATION PROCESS"
        ]
      },
      {
        "masterValue": "GRIEVANCES",
        "options": [
          "OTHER"
        ]
      }
    ],
    "partDGrievanceCMSCategories1Options": [
      {
        "masterValue": "ACCESS AND AVAILABILITY",
        "options": [
          "PHARMACY ACCESS"
        ]
      },
      {
        "masterValue": "MARKETING",
        "options": [
          "MARKETING"
        ]
      },
      {
        "masterValue": "ENROLLMENT/DISENROLLMENT",
        "options": [
          "ENROLLMENT/DISENROLLMENT"
        ]
      },
      {
        "masterValue": "QUALITY OF CARE",
        "options": [
          "QUALITY OF CARE"
        ]
      },
      {
        "masterValue": "QUALITY OF SERVICE",
        "options": [
          "CUSTOMER SERVICE"
        ]
      },
      {
        "masterValue": "POTENTIAL FRAUD/ABUSE",
        "options": [
          "OTHER"
        ]
      },
      {
        "masterValue": "BILLING/FINANCIAL DISPUTE",
        "options": [
          "OTHER"
        ]
      },
      {
        "masterValue": "CONFIDENTIALITY/PRIVACY",
        "options": [
          "OTHER"
        ]
      },
      {
        "masterValue": "BENEFIT PACKAGE",
        "options": [
          "PLAN BENEFITS"
        ]
      },
      {
        "masterValue": "APPEALS",
        "options": [
          "COVERAGE DETERMINATIONS/REDETERMINATION PROCESS"
        ]
      },
      {
        "masterValue": "GRIEVANCES",
        "options": [
          "OTHER"
        ]
      },
      {
        "masterValue": "CMS ISSUES",
        "options": [
          "CMS ISSUES"
        ]
      }
    ],
    "defaultValue": "",
    "multiselect": false
  },
  "emptyText": "",
  "iconClass": "fa clip-user-5",
  "rules": [],
  "value": "",
  "hierarchy": true,
  "childCombo": [
    "grievanceSubcategory",
    "partCCMSCategory",
    "partDGrievanceCMSCategories1"
  ],
  "oneLiner": true,
  "disabled": false,
  "listeners": {
    "change": {
      "methodName": "showGrievanceCategoryDescription",
      "param": "value"
    }
  }
}
```

###### Child Combo
```
{
  "name": "partCCMSCategory",
  "text": "Part C Grievance CMS Category <i class='fa fa-info-circle' title='CMS Universe Field'></i>",
  "dataIndex": "partCCMSCategory",
  "renderer": "",
  "width": "100px",
  "description": "Part C CMS Category",
  "type": "string",
  "tabIndex": 1,
  "tooltip": {
    "enabled": false,
    "format": null
  },
  "hidden": true,
  "mandatory": false,
  "ownerEditable": false,
  "widget": "combo",
  "hierarchy": true,
  "masterCombo": "grievanceCategory",
  "selectAllOption": true,
  "selectAllOptionText": "All",
  "properties": {
    "datasource": [
      "ACCESS",
      "MARKETING",
      "ENROLLMENT/DISENROLLMENT",
      "GRIEVANCES RELATED TO CMS ISSUES",
      "QUALITY OF CARE",
      "BENEFIT PACKAGE",
      "CUSTOMER SERVICE",
      "OTHER",
      "ORGANIZATION DETERMINATION AND RECONSIDERATION PROCESS"
    ],
    "defaultValue": "",
    "multiselect": false,
    "hierarchyOptions": [
      {
        "masterValue": "ACCESS AND AVAILABILITY",
        "options": [
          "ACCESS"
        ]
      },
      {
        "masterValue": "CMS ISSUES",
        "options": [
          "GRIEVANCES RELATED TO CMS ISSUES"
        ]
      },
      {
        "masterValue": "MARKETING",
        "options": [
          "MARKETING"
        ]
      },
      {
        "masterValue": "ENROLLMENT/DISENROLLMENT",
        "options": [
          "ENROLLMENT/DISENROLLMENT"
        ]
      },
      {
        "masterValue": "QUALITY OF CARE",
        "options": [
          "QUALITY OF CARE"
        ]
      },
      {
        "masterValue": "QUALITY OF SERVICE",
        "options": [
          "CUSTOMER SERVICE"
        ]
      },
      {
        "masterValue": "POTENTIAL FRAUD/ABUSE",
        "options": [
          "OTHER"
        ]
      },
      {
        "masterValue": "BILLING/FINANCIAL DISPUTE",
        "options": [
          "OTHER"
        ]
      },
      {
        "masterValue": "BENEFIT PACKAGE",
        "options": [
          "BENEFIT PACKAGE"
        ]
      },
      {
        "masterValue": "CONFIDENTIALITY/PRIVACY",
        "options": [
          "OTHER"
        ]
      },
      {
        "masterValue": "APPEALS",
        "options": [
          "ORGANIZATION DETERMINATION AND RECONSIDERATION PROCESS"
        ]
      },
      {
        "masterValue": "GRIEVANCES",
        "options": [
          "OTHER"
        ]
      }
    ]
  },
  "emptyText": "",
  "value": "",
  "iconClass": "fa clip-user-5",
  "rules": [],
  "listeners": {},
  "disabled": true,
  "oneLiner": true
}
```

| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "caseType" |
| text  | String  | Label for the widget | "Case Type" |
| widget  | String  | Name of the widget |  "combo" |
| oneLiner  | Boolean  | Oneliner view status | true or false |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| mandatory  | Boolean  | Mandatory status of the widget | true or false |
| tabIndex  | Number  | Tab index for the widget | true or false |
| listeners  | Object  | Contain listers information for the widget | "change": {"methodName": "update"} |
| properties.datasource  | Array  | Contain datasource for Combo | ["High", "Medium High"] |
| properties.multiselect  | Boolean  | Multiple select status for Combo | true or false |


#### Checkbox widget
```
{
  "name": "notifyUserCheckBoxGrp",
  "tabIndex": 1,
  "text": "Notify User",
  "widget": "checkboxgroup",
  "oneLiner": true,
  "mandatory": true,
  "disabled" : false,
  "hidden" : false,
  "listeners": {
    "change": {
      "methodName": "notifyUsersCheckBoxChange"
    }
  },
  "children": [
    {
      "name": "notifyUsers",
      "text": "Notify",
    },
    {
      "name": "notifyAlways",
      "text": "Notify Always",
    }
  ]
}
```

| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "notifyUserCheckBoxGrp" |
| text  | String  | Label for the widget | "Notify User" |
| widget  | String  | Name of the widget |  "checkboxgroup" |
| oneLiner  | Boolean  | Oneliner view status | true or false |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| mandatory  | Boolean  | Mandatory status of the widget | true or false |
| tabIndex  | Number  | Tab index for the widget | true or false |
| listeners  | Object  | Contain listers information for the widget | "change": {"methodName": "notifyUsersCheckBoxChange"} |
| properties.children  | Array  | Contain checkboxlist | { "name" : "notifyAlways", "text": "Notify Always"}  |

#### Button Group widget
```
{
  "name": "fetchMemberIdSearch",
  "widget": "buttonGroup",
  "cls": "fetchMemberId",
  "hidden": false,
  "disabled": false,
  "buttons": [
    {
      "name": "fetchMemberIdSearch",
      "label": "Member History",
      "hidden": true,
      "disabled": false,
      "cls": "btn btn-primary",
	  "tabIndex": 1,
      "iconClass": "fa fa-eye",
      "handler": {
        "methodName": "getMemberDetailsFromMemberId"
      }
    }
  ]
}
```

| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "fetchMemberIdSearch" |
| widget  | String  | Name of the widget |  "buttonGroup" |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| buttons  | Array  | Contain Array of button object | See the Button Object Inforamtion |

###### Button Object Inforamtion
| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the button | "fetchMemberIdSearch" |
| label  | String  | Label of the button | "Member History" |
| disabled  | Boolean  | Disabled status of the button| true or false |
| hidden  | Boolean  | Hidden status of the button | true or false |
| tabIndex  | Number  | Tab index for the button | true or false |
| cls  | String  | Class for the button | "btn btn-primary" |
| iconClass  | String  | Class for the button icon | "fa fa-eye" |
| handler  | Object  | listener for the button | {"methodName": "getMemberDetailsFromMemberId"} |

#### Datefield widget
```
{
  "name": "patientLastKnownToBeWell",
  "tabIndex": 1,
  "oneLiner": true,
  "text": "Date patient last known to be well?",
  "format": "MM-DD-YYYY",
  "requiredISODate": false,
  "allowUserToEdit": true,
  "disabled": false,
  "hidden": false,
  "mandatory": false,
  "widget": "datefield",
  "properties": {
    "defaultValue": null
  },
  "listeners": {
    "change": {
      "methodName": "patientLastKnownToBeWellChange"
    }
  },
  "buttons": [
    {
      "name": "fetchMemberIdSearch",
      "label": "Member History",
      "hidden": true,
      "disabled": false,
      "cls": "btn btn-primary",
      "tabIndex": 1,
      "iconClass": "fa fa-eye",
      "handler": {
        "methodName": "getMemberDetailsFromMemberId"
      }
    }
  ],
  "checkbox": {
    "name": "notifyUserCheckBoxGrp",
    "tabIndex": 1,
    "text": "Notify User",
    "widget": "checkboxgroup",
    "oneLiner": true,
    "mandatory": true,
    "disabled": false,
    "hidden": false,
    "listeners": {
      "change": {
        "methodName": "notifyUsersCheckBoxChange"
      }
    },
    "children": [
      {
        "name": "notifyUsers",
        "text": "Notify"
      }
    ]
  }
}
```

| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "caseType" |
| text  | String  | Label for the widget | "Case Type" |
| widget  | String  | Name of the widget |  "combo" |
| format  | String  | Moment Date format for Datefield |  "MM-DD-YYYY" |
| allowUserToEdit  | Boolean  | Edit status from keyboard |  true or false |
| requiredISODate  | Boolean  | Store ISO date string status along with date string |  true or false |
| oneLiner  | Boolean  | Oneliner view status | true or false |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| mandatory  | Boolean  | Mandatory status of the widget | true or false |
| tabIndex  | Number  | Tab index for the widget | true or false |
| listeners  | Object  | Contain listers information for the widget | "change": {"methodName": "patientLastKnownToBeWellChange"} |
| properties.defaultValue  | String  | Default value from the date widget | "03-03-1994" |
| buttons  | Array  | Contain buttonlist attached to datefield | same as buttons information from buttongroup widget |
| checkbox  | Object  | Contain checkbox information attached to datefield | same as checkbox widget information |

#### Datetimefield widget
```
{
  "name": "door_ob_INROrdered",
  "tabIndex": 1,
  "text": "INR Ordered",
  "format": "MM-DD-YYYY hh:mm:ss A",
  "requiredISODate": false,
  "oneLiner": true,
  "disabled": false,
  "hidden": false,
  "mandatory": true,
  "allowUserToEdit": true,
  "widget": "dateTimeField",
  "emptyText": "INR Ordered",
  "properties": {
    "defaultValue": null
  },
  "options": {
    "showMeridian": true
  },
  "listeners": {
    "change": {
      "methodName": "door_ob_INROrderedChange"
    }
  }
}
```

| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "door_ob_INROrdered" |
| text  | String  | Label for the widget | "INR Ordered" |
| widget  | String  | Name of the widget |  "dateTimeField" |
| format  | String  | Moment Date format for DateTimeField widget |  "MM-DD-YYYY hh:mm:ss A" |
| emptyText  | String  | Placeholder for widget |  "INR Ordered" |
| allowUserToEdit  | Boolean  | Edit status from keyboard |  true or false |
| requiredISODate  | Boolean  | Store ISO date string status along with date string |  true or false |
| oneLiner  | Boolean  | Oneliner view status | true or false |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| mandatory  | Boolean  | Mandatory status of the widget | true or false |
| tabIndex  | Number  | Tab index for the widget | true or false |
| listeners  | Object  | Contain listers information for the widget | "change": {"methodName": "door_ob_INROrderedChange"} |
| properties.defaultValue  | String  | Default value from the DateTimeField widget | null |
| options.showMeridian  | Boolean  | Meridian show status | true or false |

#### FileuploadContainer widget

```
{
  "name": "audit",
  "text": "Audit",
  "widget": "fileuploadContainer",
  "oneLiner": true,
  "tabIndex": 1,
  "displayText": "Audit Documents",
  "isVersion": true,
  "fileType": [
    "pdf",
    "jpg"
  ],
  "showDescription": true,
  "maxSize": 50,
  "mandatory": false,
  "showViewBtn": true,
  "disabled": true,
  "displayAllFile": true,
  "showDownloadBtn": true,
  "showRemoveBtn": true,
  "listeners": {
    "change": {
      "methodName": "auditChange"
    }
  }
}

```

| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "audit" |
| text  | String  | Label for the widget | "Audit" |
| widget  | String  | Name of the widget |  "fileuploadContainer" |
| oneLiner  | Boolean  | Oneliner view status | true or false |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| mandatory  | Boolean  | Mandatory status of the widget | true or false |
| tabIndex  | Number  | Tab index for the widget | true or false |
| displayText  | String  | Text for file upload modal header | "Audit Documents" |
| isVersion  | String  | Status allowing single pr multiple file upload | true or false |
| fileType  | Array  | Contain list of file types allowed to upload | ["pdf","jpg"] |
| showDescription  | Boolean  | Status for showing descriotion field in file upload modal | true or false |
| maxSize  | Number  | Maximum size allowed for uploaded file | 50 |
| showViewBtn  | Boolean  | Status for showing View button in file upload modal | true or false |
| displayAllFile  | Boolean  | Status for display all file in widget | true or false |
| showDownloadBtn  | Boolean  | Status for showing Download button in file upload modal | true or false |
| showRemoveBtn  | Boolean  |Status for showing Remove button in file upload modal | true or false |
| listeners  | Object  | Contain listers information for the widget | "change": {"methodName": "auditChange"} |

#### Grid widget

```
{
  "name": "nonMedicalGrid",
  "text": "",
  "widget": "grid",
  "cls": "nonMedicalGrid",
  "isModal": false,
  "collapsable": false,
  "columns": [
    {
      "name": "",
      "checkBoxModel": true,
      "text": "",
      "dataIndex": "",
      "width": "2%"
    },
    {
      "name": "Id",
      "serialNo": true,
      "text": "Sl No.",
      "dataIndex": "id",
      "renderer": "",
      "widget": "numberfield",
      "readOnly": true,
      "hidden": false
    },
    {
      "name": "dateNonMedical",
      "requiredISODate": true,
      "text": "Date",
      "oneLiner": false,
      "dataIndex": "dateNonMedical",
      "mandatory": false,
      "ownerEditable": false,
      "renderer": "",
      "widget": "datefield",
      "value": "",
      "properties": {
        "datasource": [],
        "defaultValue": null
      },
      "emptyText": "Date",
      "rules": [],
      "disabled": false
    },
    {
      "name": "departmentReviewStatus",
      "dataIndex": "departmentReviewStatus",
      "id": "",
      "tabIndex": 1,
      "text": "Review Status",
      "description": "Review Status",
      "type": "string",
      "tooltip": {
        "enabled": false,
        "format": null
      },
      "mandatory": false,
      "oneLiner": false,
      "widget": "combo",
      "isResetBtnVisible": false,
      "properties": {
        "datasource": [
          "Pending",
          "Response Required",
          "Complete"
        ],
        "defaultValue": "Pending"
      },
      "value": "Pending",
      "emptyText": "",
      "rules": [],
      "hidden": false,
      "disabled": true
    }
  ],
  "buttons": [
    {
      "name": "add",
      "text": "Add New",
      "type": "default-add",
      "handler": ""
    },
    {
      "name": "remove",
      "text": "Remove",
      "type": "default-remove",
      "handler": ""
    }
  ]
}
```

| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "nonMedicalGrid" |
| text  | String  | Label for the widget | "Non Medical Grid" |
| widget  | String  | Name of the widget |  "grid" |
| oneLiner  | Boolean  | Oneliner view status | true or false |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| mandatory  | Boolean  | Mandatory status of the widget | true or false |
| collapsable  | Boolean  | Collapsable status of the widget | true or false |
| isModal  | Boolean  | Open in modal status On Add or Edit rows of Grid | true or false |
| cls  | String  | External Class name for the grid | "nonMedicalGrid" |
| columns  | Array  | Containing list of widget config for each column of the grid | Same as widget config |
| buttons  | Array  | Containing list of button config for the widget |{"name": "add","text": "Add New","type": "default-add","handler": ""},|
| listeners  | Object  | Contain listers information for the widget | "change": {"methodName": "auditChange"} |

#### Notification Widget

```
{
   "name":"note_name",
   "text":"Note! Opened and selected nodes will be saved in the user's browser, so when returning to the same tree the previous state will be restored.",
   "hidden":false
   "cls":"alert"
   "widget":"note"
}
```
| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "note_name" |
| text  | String  | Label for the widget | "Note! Opened and selected nodes will be saved in the user's browser, so when returning to the same tree the previous state will be restored." |
| widget  | String  | Name of the widget |  "note" |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| cls  | String  | External Class name for the wodget | "alert" |

#### Numberfield Widget
```
{
  "name": "incidentId",
  "text": "Incident ID",
  "oneLiner": true,
  "type": "number",
  "mandatory": true,
  "widget": "numberfield",
  "emptyText": "Incident ID",
  "pattern": "[0-9]",
  "range": [
    10.5,
    12.4
  ],
  "decimalPrecisionValue": 3,
  "hidden": true,
  "disabled": false,
  "spellcheck": true,
  "listeners": {
    "change": {
      "methodName": "update"
    },
    "keyup": {
      "methodName": "update"
    },
    "click": {
      "methodName": "update"
    }
  }
}
```
| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "incidentId" |
| text  | String  | Label for the widget | "Incident ID" |
| widget  | String  | Name of the widget |  "numberfield" |
| oneLiner  | Boolean  | Oneliner view status | true or false |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| mandatory  | Boolean  | Mandatory status of the widget | true or false |
| cls  | String  | External Class name for the grid | "nonMedicalGrid" |
| emptyText  | String  | Placeholder for the widget | "Incident ID" |
| pattern  | String  | Input Pattern for the widget | "[0-9]" |
| range  | String  | Range of input for the widget | "[10.5, 12.4]" |
| decimalPrecisionValue  | Number  | Number of precesion after decimal for the widget | 3 |
| spellcheck  | Boolean  | Spell check status for the widget | true or false |
| listeners  | Object  | Contain listers information for the widget | "change": {"methodName": "incidentIdChange"} |

#### Radiogroup Widget
```
{
  "name": "isActionTaken",
  "tabIndex": 1,
  "text": "Is Action Taken",
  "oneLiner": true,
  "mandatory": true,
  "hidden": false,
  "widget": "radio",
  "properties": {
    "datasource": [
      "Yes",
      "No"
    ],
    "defaultValue": "No"
  },
  "listeners": {
    "change": {
      "methodName": "update"
    }
  }
}
```

| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "isActionTaken" |
| text  | String  | Label for the widget | "Is Action Taken" |
| widget  | String  | Name of the widget |  "radio" |
| oneLiner  | Boolean  | Oneliner view status | true or false |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| mandatory  | Boolean  | Mandatory status of the widget | true or false |
| properties.datasource  | Array  | Contain datasource item | ["Yes", "No"] |
| properties.defaultValue  | String  | Contain default value for widget | "No" |
| listeners  | Object  | Contain listers information for the widget | "change": {"methodName": "isActionTakenChage"} |

#### Richtext Editor widget

```
{
  "name": "textEditor",
  "text": "Text Editor",
  "hidden": "false",
  "oneLiner": "true",
  "mandatory": true,
  "widget": "textEditor",
  "disabled": false,
  "spellcheck": true,
  "encode": true
}
```

| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "textEditor" |
| text  | String  | Label for the widget | "Text Editor" |
| widget  | String  | Name of the widget |  "radio" |
| oneLiner  | Boolean  | Oneliner view status | true or false |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| mandatory  | Boolean  | Mandatory status of the widget | true or false |
| listeners  | Object  | Contain listers information for the widget | "change": {"methodName": "textEditorChange"} |

#### Textarea widget

```
{
  "name": "caseShortDescription",
  "text": "Case Short Description",
  "mandatory": true,
  "widget": "textarea",
  "maxlength": 100,
  "minlength": 10,
  "emptyText": "Case Short Description",
  "rows": "30",
  "cols": "40",
  "disabled": true,
  "readonly": true,
  "oneLiner": true,
  "tabindex": 1,
  "spellcheck": true,
  "wrap": "off",
  "modalView": true,
  "listeners": {
    "change": {
      "methodName": "update"
    },
    "keyup": {
      "methodName": "update"
    },
    "click": {
      "methodName": "update"
    }
  }
}
```
| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "caseShortDescription" |
| text  | String  | Label for the widget | "Case Short Description" |
| widget  | String  | Name of the widget |  "textarea" |
| oneLiner  | Boolean  | Oneliner view status | true or false |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| mandatory  | Boolean  | Mandatory status of the widget | true or false |
| maxlength  | Number  | Maxlength for the widget | 100 |
| minlength  | Number  | Minlength for the widget | 10 |
| emptyText  | String  | Placeholder for the widget | "Case Short Description" |
| rows  | String  | Number of rows for textarea | "30" |
| cols  | String  | Number of columns for textarea | "30" |
| wrap  | String  | Wrap status of the widget | "on" or "off" |
| spellcheck  | Boolean  | Spellcheck status of the widget | true or false |
| modalView  | Boolean  | Modal view status of the widget | true or false |
| readonly  | Boolean  | Readonly proerty of the widget | true or false |
| listeners  | Object  | Contain listers information for the widget | "change": {"methodName": "caseShortDescriptionChange"} |

#### Textfield widget

```
{
  "name": "incidentId",
  "text": "Incident ID",
  "oneLiner": true,
  "type": "string",
  "maxsearchlength": 500,
  "minlength": 10,
  "mandatory": true,
  "widget": "textfield",
  "emptyText": "Incident ID",
  "pattern": "[6789]",
  "range": [
    10.5,
    12.4
  ],
  "decimalPrecisionValue": 3,
  "hidden": true,
  "disabled": false,
  "spellcheck": true,
  "countryCode": "IN",
  "listeners": {
    "change": {
      "methodName": "update"
    },
    "keyup": {
      "methodName": "update"
    },
    "click": {
      "methodName": "update"
    }
  },
  "buttons": [
    {
      "name": "fetchMemberIdSearch",
      "label": "Member History",
      "hidden": true,
      "disabled": false,
      "cls": "btn btn-primary",
      "tabIndex": 1,
      "iconClass": "fa fa-eye",
      "handler": {
        "methodName": "getMemberDetailsFromMemberId"
      }
    }
  ],
  "checkbox": {
    "name": "notifyUserCheckBoxGrp",
    "tabIndex": 1,
    "text": "Notify User",
    "widget": "checkboxgroup",
    "oneLiner": true,
    "mandatory": true,
    "disabled": false,
    "hidden": false,
    "listeners": {
      "change": {
        "methodName": "notifyUsersCheckBoxChange"
      }
    },
    "children": [
      {
        "name": "notifyUsers",
        "text": "Notify"
      }
    ]
  }

}
```

| Properties  | Type | Description | Example |
| ----------  | ---- | ----------- | ------- |
| name  | String  | Name of the widget | "incidentId" |
| text  | String  | Label for the widget | "Incident ID" |
| type  | String  | Type of input for the widget | "string", "number" |
| minlength  | Number  | Minlength for the widget | 10 |
| maxsearchlength  | Number  | Maxsearch length for the widget | 500 |
| widget  | String  | Name of the widget |  "textfield" |
| oneLiner  | Boolean  | Oneliner view status | true or false |
| disabled  | Boolean  | Disabled status of the widget| true or false |
| hidden  | Boolean  | Hidden status of the widget | true or false |
| mandatory  | Boolean  | Mandatory status of the widget | true or false |
| cls  | String  | External Class name for the grid | "nonMedicalGrid" |
| emptyText  | String  | Placeholder for the widget | "Incident ID" |
| pattern  | String  | Input Pattern for the widget | "[0-9]" |
| range  | String  | Range of input for the widget | "[10.5, 12.4]" |
| decimalPrecisionValue  | Number  | Number of precesion after decimal for the widget | 3 |
| spellcheck  | Boolean  | Spell check status for the widget | true or false |
| countryCode  | String  | Contrycode for phonenumber validation | true or false |
| buttons  | Array  | Contain buttonlist attached to textfield | same as buttons information from buttongroup widget |
| checkbox  | Object  | Contain checkbox information attached to textfield | same as checkbox widget information |
| listeners  | Object  | Contain listers information for the widget | "change": {"methodName": "incidentIdChange"} |
