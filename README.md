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

		"list":["Mouth_comp_101", "Section_comp_102"],

		"parameters":{

		    "Mouth_comp_101":{
			"name":"Mouth",
			"display_name":"Mouth",
			"uid":"101",
			"id":0,
			"interactable":true,
			"viewable":true,
			"description":"",
			"submodule_name":"Teeth_mod_201"
		    }
		    ,
		    "Section_comp_102":{
			"name":"Section",
			"display_name":"Section",
			"uid":"102",
			"id":1,
			"interactable":true,
			"viewable":true,
			"description":"",
			"submodule_name":"Tooth_mod_202"
		    }

		}
	}
	,

	"module_data":{
		"list":["Teeth_mod_201", "Tooth_mod_202"],

	        "parameters":{
	            "Teeth_mod_201":{
	                "name":"Teeth",
	                "uid":"201",
	                "submodule_data":{
	                    "list":["open_sub_308", "nerve_sub_309"],
	                    "parameters":{
	                        "open_sub_308":{
	                            "name":"open",
	                            "uid":"308",
	                            "clickable":true
	                        },
	                        "nerve_sub_309":{
	                            "name":"nerve",
	                            "uid":"309",
	                            "clickable":true
	                        }
	                    }
	                }
	            },
	
	            "Tooth_mod_202":{
	                "name":"Tooth",
	                "uid":"202",
	                "submodule_data":{
	                    "list":["nerve_sub_301", "gum_sub_302", "dentin_sub_303", "nerve_sub_304", "tooth_sub_305", "half_tooth_sub_306", "nerve_sub_307"],
	
	                    "parameters":{
	                        "nerve_sub_301":{
	                            "name":"nerve",
	                            "uid":"301",
	                            "clickable":true
	                        },
	                        "gum_sub_302":{
	                            "name":"gum",
	                            "uid":"302",
	                            "clickable":true
	                        },
	                        "dentin_sub_303":{
	                            "name":"dentin",
	                            "uid":"303",
	                            "clickable":true
	                        },
	                        "nerve_sub_304":{
	                            "name":"nerve",
	                            "uid":"304",
	                            "clickable":true
	                        },
	                        "tooth_sub_305":{
	                            "name":"tooth",
	                            "uid":"305",
	                            "clickable":true
	                        },
	                        "half_tooth_sub_306":{
	                            "name":"half-tooth",
	                            "uid":"306",
	                            "clickable":true
	                        },
	                        "nerve_sub_307":{
	                            "name":"nerve",
	                            "uid":"307",
	                            "clickable":true
	                        }
	                    }
	                }
	            }
	
	        }
	}

}
```

