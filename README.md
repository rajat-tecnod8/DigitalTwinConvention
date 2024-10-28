# DigitalTwinConvention

The platform currently supports 3 levels of simulation of a object.
Taking the teeth copilot for example, the levels would be,
level 1 - mouth
level 2 - an individual tooth
level 3 - nerves inside the tooth

We call the level 1 view as "components", level 2 as "modules" and level 3 as "submodules". 

The naming convention for the 3D object would be,
```
component:
	<name>_comp_<cid>
	eg. "box_comp_001"

module:
	<name>_mod_<cid>_<id>
	eg. "board_mod_001"

submodule:
	<name>_sub_<cid>_<id>
	eg. "flap_sub_001_002"
```

We would have to make a json file for the parameters of the object.
Eg.
```json
{
	"component_data":{

		"list":["abc_comp_001", "def_comp_002"],

		"parameters":{

			"abc_comp_001":{
			 	"name":"abc",
				"display_name":"abc",
                		"id":"001",
				"interactable":true,
                		"viewable":true,
				"description":" ",
				"module_name":" "	
			 }

		}
	}
	,

	"module_data":{
		"list":["abc_mod_001", "def_mod_002"],

        "parameters":{

            "abc_mod_001":{
                "name":"abc",
                "submodule_data":{
                    "list":["ab_sub_001_01", "cd_sub_001_02"],
                    "parameters":{
                        "ab_sub_001_01":{
                            "name":"cde",
                            "clickable":true
                        },

                        "cd_sub_001_02":{
                            "name":"def",
                            "clickable":true
                        }
                    }
                }
            },

            "def_mod_002":{
                "name":"def",
                "submodule_data":{
                    "list":["ab_sub_002_01", "cd_sub_002_02"],
                    "parameters":{
                        "ab_sub_002_01":{
                            "name":"cde",
                            "clickable":true
                        },

                        "cd_sub_002_02":{
                            "name":"def",
                            "clickable":true
                        }
                    }
                }
            }

        }
	}

}
```

