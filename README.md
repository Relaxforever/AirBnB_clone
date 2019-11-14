# 0x00. AirBnB clone - The console
---
<img align="center"
src="https://secure.meetupstatic.com/photos/event/b/c/5/6/highres_475548214.jpeg"
width="100%"/>

## Airbnb Clone - Command Interpreter
---
This is the Part One of a project working towards building a full web
application like the AirBnB.
In this part, Python is used to build a command interpreter for the clone's web
app. This interpreter will be build like a cmd or shell/bash interpreter, so you
can interactibly make changes, create, destroy and show different instances of
an object, be like User/Amenity/Place, etc.

### How To execute it
---
##### Linux
To begin using this repository you can use clone this way
`git clone https://github.com/Relaxforever/AirBnB_clone.git`
then you can acces the repository using 
`cd AirBnB_clone`
and then when you want to start it execute the following command
`./console.py`

### Files
---
File Name | Description
--- | ---
`models/base_model.py` | Base Class that will be used as a father to most utility classes
`models/state.py` | A state class that has the name of the state inherits from BaseModel
`models/city.py` | A city class that has the name of the city, inherits from BaseModel
`models/user.py` | A user class that has all user information, inherits from BaseModel
`models/place.py` | A place class that has all the information about the house/apartment/home, inherits from BaseModel
`models/review.py` | A review class that let's the user leave a review of the place, inherits from BaseModel
`models/amenity.py` | An amenity class that has all amenity information, inherits from BaseModel
`models/engine/file_storage.py` | A class that get's to serialize instances to a JSON file and deserializes JSON file to instances
`tests/test_models/` | The unittest files for all the previous Classes
`tests/test_models/test_engine/` | Unittest for the way we Storage File/File Storager

### Usage
---

This interpreter has basic console commands

Command | Syntax | Output
------- | ------ | ------
help | `help *[option]*` | Lists all current avaliable commands, or shows what a commands does
quit | `quit` | Exit command interpreter
EOF | `EOF` | Exit command interpreter
create | `create [class_name]` or `[class_name].create()`| Creates an instance of the given name class
update | `update [class_name] [object_id] [update_key] [update_value]` or
`[class].update([object_id] [update_key] [update_value]()`| Updates the key:value of class_name.object_id instance
show | `show [class_name] [object_id]` or `[class_name].show([object_id])()` | Displays all attributes of class_name.object_id
all | `all [class_name]`, `[class_name].all()` | Displays every instance of class_name, if used without option displays every instance saved to the file
destroy | `destroy [class_name] [object_id]` or
`[class_name].destroy([object_id])()` | Deletes all attributes of class_name.object_id
## Example Usage
---
```python3
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  all  count  create  destroy  help  quit  show  update

(hbnb) create City
4186038f-0266-42d4-bdb4-f8be14409b5c
(hbnb) all
[City] (4186038f-0266-42d4-bdb4-f8be14409b5c) {'updated_at':
datetime.datetime(2019, 11, 14, 3, 8, 41, 196420), 'created_at':
datetime.datetime(2019, 11, 14, 3, 8, 41, 195792), 'id':
'4186038f-0266-42d4-bdb4-f8be14409b5c'}
(hbnb) update City 4186038f-0266-42d4-bdb4-f8be14409b5c name El Paso
(hbnb) show City 4186038f-0266-42d4-bdb4-f8be14409b5c
[City] (4186038f-0266-42d4-bdb4-f8be14409b5c) {'id':
'4186038f-0266-42d4-bdb4-f8be14409b5c', 'name': 'El Paso', 'created_at':
datetime.datetime(2019, 11, 14, 3, 8, 41, 195792), 'updated_at':
datetime.datetime(2019, 11, 14, 3, 8, 41, 196420)}
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  all  create  destroy  help  quit  show  update

(hbnb) quit
```


Authors:
* **Juan Diego Arango Piedrahita** -  [Jdarangop](https://github.com/jdarangop)
* **Fidel Fernando Caicedo Castaño** - [Relaxforever](https://github.com/Relaxforever)
