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
	title: 'Expedite',
	id: 'showExpediteCaseBtn',
	root: true,
	page: '/feature/6100/inbox',  OR onClick: 'getExpediteCaseNotification',
	alignment: 'left',
	icon: 'fa fa-bell',
	target: '_self',
	
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
