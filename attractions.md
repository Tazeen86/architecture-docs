            #Attractions
            
            Key Name |Data Type|Description|Example
            images |array | Set of image names with path example | [/{user_id}/{yyyy}/{mm}/{dd}/{filename}.{extension}] |
            default_image | integer | array index | 0 
            title |string | title of the event | Cat grooming sessions
            attraction_category |array | the active audience category types | [10,12,13]
            description  |string | description of the event | How to groom your cat efficiently
            start_time  | integer | UTC Epoch | 1675099193000
            excludes_sunday |integer| 1 if sunday excluded and 0 if sunday included| 0/1
            is_on_weekends |integer| 1 if attraction is on weekends 0 if not on weekends| 0/1
            end_time_attractions | integer | end time| 1675099193000 
            location | object | lat and long object | {lat: 10.0, lng: 20.0}
            geolocated_address|string | geolocated address from the google APIs | b402, Neel Sidhi Ornate, Kharghar, Mumbai
            payment_type |integer | payment type of the activity if the activity is paid or else unpaid | set 0 if the payment type is 0 or else 1
            venue| string| whether outdoor or indoor | "Indoor"/"Outdoor"
            attraction_status |integer| 0 for deleted attraction/ cancelled attraction |0/1 


           #request in json
           
                         {
                "images": [
                  "10/2023/01/30/a.jpg",
                  "10/2023/01/30/b.jpg"
                ],
                "default_image": 1,
                "title": "Blue Mosque",
                "attraction_category": [
                  1,
                  2,
                  3,
                  4
                ],
                "attraction_status":1,
                "description": "turkish beauty",
                "start_time": 1675231560,
                "end_time_attractions":1675231560,
                "venue":"Test",


                "location": {
                  "lat": -37.144,
                  "lng": 140.44
                },
                "geolocated_address": "b402, Neel Sidhi Ornate, Kharghar, Mumbai",
                "payment_type": 1
              }
              
              
              #response in json
                   {
                      "success": true,
                      "message": "attraction created successfully",
                      "data": "{'uuid': '67b4dd61-8c43-4fb6-9f3b-5c36344b0fb1'}"
                  }
                  
             #api endpoints
             
             create | POST | /attraction
             update | PUT |/attraction
             get | GET |/attraction
             delete |DEL| /attraction
