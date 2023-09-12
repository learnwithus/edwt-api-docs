# Emergency Department Wait Times API
The Emergency Wait Times API allows up to date infromation regarding EDs to be pushed in realtime to EDWT website.

## `POST` @ `/api/report`

```js
{
	"token": "password",  // This token string is used to authenticate the request

	// waitTimes is an array of objects that describes the locations which you have new wait times for
	"waitTimes": [
		{
			"locationSlug": "vgh", // The slug string used to identify the location
			"waitTimeMinutes": 83, // A number or null representing the current wait time in minutes
			"elosMinutes": 144, // A number or null representing the current expected length of stay in minutes
			"status": "normal" // A string enum that is either "normal" or "abnormal" to represent current status
		},
		...
	]    

}

```
