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
	name_comp_id
	eg. "box_comp_001"

module:
	name_mod_<cid>
	eg. "board_mod_001"

submodule:
	name_sub_<cid>_id
	eg. "flap_sub_001_002"
```

We would have to make a json file for the parameters of the object.
Eg.
```json
{
	"component_data":{

		"components":["abc_comp_001", "def_comp_002"],

		"parameters":{

			"abc_comp_001":{
			 	"name":"abc",
				"display_name":"abc",
				"interactable":false	
			 },
			
			"def_comp_002":{
				"name":"cde",
				"display_name":"efg",
				"interactable":true	
			}
		}
	}
	,

	"module_data":{
		"modules":["abc_mod_001", "def_mod_002"],

        "parameters":{

        }
	}
	,
	"submodule_data":{
		"submodules":["ab_sub_001_01", "cd_sub_001_02"],

        "parameters":{

        }
	}

}
```

