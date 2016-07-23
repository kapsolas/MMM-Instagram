# MMM-Instagram
This a module for the [MagicMirror](https://github.com/MichMich/MagicMirror/tree/develop). It pulls photos from your own or another users Instagram feed (requires API_KEY). The photos are then rotated and animated in the screen.

## Installation
1. Navigate into your MagicMirror's `modules` folder and execute `git clone https://github.com/kapsolas/MMM-Instagram.git`. A new folder will appear, navigate into it.
2. Execute `npm install` to install the node dependencies.

## Config
The entry in `config.js` can include the following options:


{
            module: 'MMM-Instagram',
            position: 'top_left',
            config: {
                access_token: '1160247792.b119586.49fa97770ee34deb92e621069c760cee',
                count: 200,
                min_timestamp: 0,
                animationSpeed: 2500,
                updateInterval: 12000
            }


|Option|Description|
|---|---|
|`access_token`|Access token which is received from Instagram<br><br>**Type:** `string`<br>This value is **REQUIRED**|
|`count`|Number of pictures to pull from the feed.<br><br>This value is **REQUIRED**|
|`min_timestamp`|Set to 0 to pull images from when you created the account.<br><br>This value is **REQUIRED**|
|`animationSpeed`|How long the fade out and fade in of photos should take.<br><br>This value is **REQUIRED**|
|`updateInterval`|How long before refreshing image list.<br><br>This value is **REQUIRED**|

Here is an example of an entry in `config.js`
```
{
	module: 'MMM-Instagram',
	position: 'top_right',
	config: {
		access_token: 'API_KEY from instagram',
		count: 200,  
		min_timestamp: 0,
		animationSpeed: 2500,
		updateInterval: 12500
	}
},
```

## Dependencies
- [request](https://www.npmjs.com/package/request) (installed via `npm install`)

## Important Notes
- This is one of my first projects using Node, so feel free to submit pull requests or post on the issues/wiki and I will do my best to improve the project.

## Special Thanks
- [Michael Teeuw](https://github.com/MichMich) for creating the awesome [MagicMirror2](https://github.com/MichMich/MagicMirror/tree/develop) project that made this module possible.
- [Sam Lewis](https://github.com/SamLewis0602/) for creating the [MMM-Traffic](https://github.com/SamLewis0602/MMM-Traffic) module that I used as guidance in creating this module.
