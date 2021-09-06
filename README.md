# PowerAppsWithBingMap

Youtube Video for your Refrence : https://www.youtube.com/watch?v=QXsYA4NDqWQ&t=2s
Blog for your Reference : https://microsoftcrmtechie.blogspot.com/2021/09/powerapps-with-bing-maps.html

Default for Label 1 : Location.Latitude
Default for Label 2 : Location.Longitude

Load Image Based on Current Latitude and Longitude

BingMaps.GetMap("Road",15,Location.Latitude,Location.Longitude)

Load Location based on Dynamic Values

 OnSelect of Button Set(getLocationByAddress,BingMaps.GetLocationByAddress({addressLine:TextInput1.Text,adminDistrict:TextInput1_1.Text,postalCode:TextInput1_2.Text}))
 
 TextInput1 --> Input Value 1
 TextInput1_1 --> Input Value 2
 TextInput1_2 --> Input Value 3
 
 To load Dynamic Values Paste the Below Code
 
 BingMaps.GetMap("Road",15,getLocationByAddress.point.coordinates.latitude,getLocationByAddress.point.coordinates.longitude,{pushpin:getLocationByAddress.point.coordinates.latitude&","&getLocationByAddress.point.coordinates.longitude&";21;"& TextInput1.Text})

"Road" --> Road View
15 --> Zoom Level
getLocationByAddress.point.coordinates.latitude --> Latitude
getLocationByAddress.point.coordinates.longitude --> Longitude
PushPin{} --> for Showing push pin with Comma separator with Latitude and Longitude
21--> Map with Pushpin number
TextInput1.Text --> To display address

