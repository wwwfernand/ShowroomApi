# ShowroomApi

**API** for [showroom-live.com](https://www.showroom-live.com/)

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'showroom_api'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install showroom_api

## Usage

Data can be obtained using the following patterns:

    > ::ShowroomApi::Live.onlives
    > ::ShowroomApi::Live.live_info(room_id)
    > ::ShowroomApi::Room.profile(room_id)
    > ::ShowroomApi::User.profile(user_id)


## Commands

* **Live**

  Contains info of currently onlive stream
  | Method | Argument | Definition | 
  | :------------- |:-------------:| :-----|
  | onlives | size(optional) | Array of room categories and their available live rooms.<br>Return all the info or just part if size is provided |
  | live_info | room_id | Info of the room |
  | streaming_url | room_id | List of room's streaming URLs |
  | polling | room_id | Live status of the room  |
  | age_verification | room_id | - |
  | current_user | room_id | Logged in user's info <small>(#1)</small> |
  | telop | room_id | - |
  | enquete_result | room_id | Room's survey result |
  | summary_ranking | room_id | Room's ranking summary |
  | comment_log | room_id | Room's comment log |
  | gift_log | room_id | Room's gift log |
  | gift_list | room_id | Room's available gift |
  | stage_gift_list | room_id | List of gifts the room received |
  | stage_user_list | room_id | List of users in the room |
  | onlive_num | - | Count of currently available rooms |

* **Room**

  Contains info of a room
  | Method | Argument | Definition |
  | ------------- |:-------------:| :-----|
  | event_and_support | room_id | Info about event and support of the room |
  | profile | room_id | Profile info of the room |
  | next_live | room_id | Room's next live schedule |
  | settings | room_id | Rooms available performance |
  | status | room_id | Status of the room |

* **User**
  
  Contains info of a user
  | Method | Argument | Definition |
  | ------------- |:-------------:| -----:|
  | profile | user_id | Profile info of the user |
  | detail | user_id | Detailed info of the logged-in user <small>(#1)</small> |

	<small>(#1) Needs to be logged-in</small>

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/wwwfernand/showroom_api.

