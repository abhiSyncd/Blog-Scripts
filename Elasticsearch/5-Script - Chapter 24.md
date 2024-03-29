

## 1-Create Index 

PUT /restaurants/

## 2-Create Mapping

    PUT /restaurants/_mapping
    {
      "properties": {
          "hotel_name"     : {  "type": "text"}, 


          "hotel_region"   : {  "type": "text" },


          "hotel_menu"     : {
             "type": "nested",
             "properties": {
                "food_category"     : {"type": "text" },
                "food_items" :{
                    "type": "nested",               
                    "properties": {
                       "food_name"        : {"type": "text" },
                       "food_unit_price"  : {"type": "float" }
                    }
                 }  
              }
          }, 


          "isPureVeg"       : {"type": "boolean"}, 


          "isOnlinePaymentAvailable" : {"type": "boolean"},


          "rating"          : {"type": "float"}

       }
    }

## 3-Insert Documents


    PUT restaurants/_doc/1
    {
      "hotel_name": "Modak- (Bellandur-Region + Have-Paneer + Pure-Veg, Online-Payment-Available)",
      "hotel_region": "Bellandur",
      "hotel_menu": [
        {
          "food_category": "STARTERS",
          "food_items": [
            {
              "food_name": "Green salad",
              "food_unit_price": 20
            },
            {
              "food_name": "Paneer Chilly",
              "food_unit_price": 50
            }
          ]
        },
        {
          "food_category": "MAIN_COURSE",
          "food_items": [
            {
              "food_name": "Shahi Paneer Kadhai",
              "food_unit_price": 100
            },
            {
              "food_name": "Veg Biryani",
              "food_unit_price": 150
            }
          ]
        }
      ],
      "isPureVeg": "true",
      "isOnlinePaymentAvailable": "true",
      "rating": 4.6
}

#

    PUT restaurants/_doc/2
    {
      "hotel_name": "Murli- (Bellandur-Region + Have-Paneer + Pure-Veg, Online-Payment-Available)",
      "hotel_region": "Bellandur",
      "hotel_menu": [
        {
          "food_category": "STARTERS",
          "food_items": [
            {
              "food_name": "Sammosa",
              "food_unit_price": 20
            },
            {
              "food_name": "Puri Sabzi",
              "food_unit_price": 50
            }
          ]
        },
        {
          "food_category": "MAIN_COURSE",
          "food_items": [
            {
              "food_name": "Paneer Butter Masala",
              "food_unit_price": 100
            },
            {
              "food_name": "Veg Biryani",
              "food_unit_price": 150
            }
          ]
        }
      ],
      "isPureVeg": "true",
      "isOnlinePaymentAvailable": "true",
      "rating": 3.9

    }

#

    PUT restaurants/_doc/3
    {
      "hotel_name": "Lassi Shop- (Bellandur-Region + Have-Paneer + Pure-Veg, Online-Payment-Available)",
      "hotel_region": "Bellandur",
      "hotel_menu": [
        {
          "food_category": "STARTERS",
          "food_items": [
            {
              "food_name": "Paneer cheese sandwich",
              "food_unit_price": 100
            },
            {
              "food_name": "Puri Sabzi",
              "food_unit_price": 50
            }
          ]
        },
        {
          "food_category": "MAIN_COURSE",
          "food_items": [
            {
              "food_name": "Mushroom Masala",
              "food_unit_price": 100
            },
            {
              "food_name": "Veg Biryani",
              "food_unit_price": 150
            }
          ]
        }
      ],
      "isPureVeg": "true",
      "isOnlinePaymentAvailable": "true",
      "rating": 3.7
    }


# 

    PUT restaurants/_doc/4
    {
      "hotel_name": "S Popular Frozen Stone - (Bellandur-Region + Have-Paneer + Pure-Veg, Online-Payment-Available)",
      "hotel_region": "Bellandur",
      "hotel_menu": [
        {
          "food_category": "STARTERS",
          "food_items": [
            {
              "food_name": "Paneer cheese sandwich",
              "food_unit_price": 100
            },
            {
              "food_name": "VEG Roll",
              "food_unit_price": 50
            }
          ]
        },
        {
          "food_category": "MAIN_COURSE",
          "food_items": [
            {
              "food_name": "Daal Tadka",
              "food_unit_price": 100
            },
            {
              "food_name": "Veg Biryani",
              "food_unit_price": 150
            }
          ]
        }
      ],
      "isPureVeg": "true",
      "isOnlinePaymentAvailable": "true",
      "rating": 3.1
    }


#

    PUT restaurants/_doc/5
    {
      "hotel_name": "Flying Cup - (Bellandur-Region + Have-Paneer + Not-Pure-Veg + No-Online-Payment-Available)",
      "hotel_region": "Bellandur",
      "hotel_menu": [
        {
          "food_category": "STARTERS",
          "food_items": [
            {
              "food_name": "Paneer Sticks",
              "food_unit_price": 20
            },
            {
              "food_name": "Paneer Balls",
              "food_unit_price": 50
            }
          ]
        },
        {
          "food_category": "MAIN_COURSE",
          "food_items": [
            {
              "food_name": "Veg Pulaow",
              "food_unit_price": 100
            },
            {
              "food_name": "Veg Biryani",
              "food_unit_price": 150
            }
          ]
        }
      ],
      "isPureVeg": "true",
      "isOnlinePaymentAvailable": "true",
      "rating": 2.5
    }



#

    PUT restaurants/_doc/6
    {
      "hotel_name": "Fresh Menu - (Bellandur-Region + Have-Paneer + Not-Pure-Veg +  Online-Payment-Available)",
      "hotel_region": "Bellandur",
      "hotel_menu": [
        {
          "food_category": "STARTERS",
          "food_items": [
            {
              "food_name": "Paneer Bhurji",
              "food_unit_price": 20
            },
            {
              "food_name": "Chicken Lollypop",
              "food_unit_price": 50
            }
          ]
        },
        {
          "food_category": "MAIN_COURSE",
          "food_items": [
            {
              "food_name": "Veg Biryani",
              "food_unit_price": 100
            },
            {
              "food_name": "Chicken Biryani",
              "food_unit_price": 150
            }
          ]
        }
      ],
      "isPureVeg": "false",
      "isOnlinePaymentAvailable": "true",
      "rating": 3.7
    }


#

    PUT restaurants/_doc/7
    {
      "hotel_name": "Tipsy Bull  - (Bellandur-Region +  No-Paneer + Not-Pure-Veg + Online-Payment-Available)",
      "hotel_region": "Bellandur",
      "hotel_menu": [
        {
          "food_category": "STARTERS",
          "food_items": [
            {
              "food_name": "Garlic Mushroom",
              "food_unit_price": 20
            },
            {
              "food_name": "Pasta",
              "food_unit_price": 50
            }
          ]
        },
        {
          "food_category": "MAIN_COURSE",
          "food_items": [
            {
              "food_name": "Chicken curry with Dosa",
              "food_unit_price": 100
            },
            {
              "food_name": "Chicken Biryani",
              "food_unit_price": 150
            }
          ]
        }
      ],
      "isPureVeg": "false",
      "isOnlinePaymentAvailable": "true",
      "rating": 3.5
    }

#

    PUT restaurants/_doc/8
    {
      "hotel_name": "Srinathji's - (Bellandur-Region + Have-Paneer + Not-Pure-Veg + No-Online-Payment-Available)",
      "hotel_region": "Bellandur",
      "hotel_menu": [
        {
          "food_category": "STARTERS",
          "food_items": [
            {
              "food_name": "Paneer Sticks",
              "food_unit_price": 20
            },
            {
              "food_name": "Chicken Balls",
              "food_unit_price": 50
            }
          ]
        },
        {
          "food_category": "MAIN_COURSE",
          "food_items": [
            {
              "food_name": "Chicken curry with Dosa",
              "food_unit_price": 100
            },
            {
              "food_name": "Chicken Biryani",
              "food_unit_price": 150
            }
          ]
        }
      ],
      "isPureVeg": "false",
      "isOnlinePaymentAvailable": "false",
      "rating": 5.0
    }


#

    PUT restaurants/_doc/9
    {
      "hotel_name": "Hot and Cold Bakery - (Not In Bellandur region)",
      "hotel_region": "BTM",
      "hotel_menu": [
        {
          "food_category": "STARTERS",
          "food_items": [
            {
              "food_name": "ww",
              "food_unit_price": 20
            },
            {
              "food_name": "xx",
              "food_unit_price": 50
            }
          ]
        },
        {
          "food_category": "MAIN_COURSE",
          "food_items": [
            {
              "food_name": "yy",
              "food_unit_price": 100
            },
            {
              "food_name": "zz",
              "food_unit_price": 150
            }
          ]
        }
      ],
      "isPureVeg": "false",
      "isOnlinePaymentAvailable": "false",
      "rating": 5.0
    }
