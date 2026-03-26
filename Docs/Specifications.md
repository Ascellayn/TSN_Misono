# Documentation to create Misono CSS Modules

### File Tree Example
Warning: CSS Files are read and compiled **in alphabetical order**.
```
MyModule/
	Floating/
		- Main.css
	Fullscreen/
		- Main.css
	- Worshipper.json
```

### Worshipper JSON (Module)
```json
{
	"Info": {
		"Name": "My Module",
		"Internal": "MyModule", # [a-zA-Z_]
		"Description": "", # Can be markdown
	},
	"Module": {
		"Compatibility": {
			"Dependencies": {
				"Hard": [
					"MyRequired_Addon"
				],
				"Soft": [
					"MyImprovementAddon+VariantTwo"
				]
			}
		},
		"Variants": [
			"Floating", # Must correspond to a folder, First option is the default
			"Fullscreen" # This would be known internally as MyModule+Fullscreen
		],
		"Settings": [
			[
				"--FixedSelection", # CSS Variable
				"Description of Setting", # Can be markdown
				["8px", "16px", "24px"] # List of options
			],
			[
				"--Username",
				"Free selection",
				"[a-zA-Z_-]" # Regex
			]
		]
	}
}
```

### Worshipper JSON (Addon)
```json
{
	"Info": {
		"Name": "My Module",
		"Internal": "MyModule", # [a-zA-Z_]
		"Description": "", # Can be markdown
		"Version": [2026, 3, 22],
		"Authors": ["Ascellayn"],
		"License": "TSN License 2.1 Strict",
		"License_URL": "https://sirio-network.com/license/2.1",
		"Socials": {
			"Discord": "https://sirio-network.com/discord",
			"GitHub": "https://github.com/Ascellayn/TSN_Misono"
		}
	},
	"Module": {
		"Compatibility": {
			"Misono_Branch": 0, # See Misono Branches
			"Misono_Version": [2026, 3, 22],
			"Dependencies": {
				"Hard": [
					"MyRequired_Addon"
				],
				"Soft": [
					"MyImprovementAddon+VariantTwo"
				]
			}
		},
		"Variants": [
			"Floating", # Must correspond to a folder, First option is the default
			"Fullscreen" # This would be known internally as MyModule+Fullscreen
		],
		"Settings": [
			[
				"--FixedSelection", # CSS Variable
				"Description of Setting", # Can be markdown
				["8px", "16px", "24px"] # List of options
			],
			[
				"--Username",
				"Free selection",
				"[a-zA-Z_-]" # Regex
			]
		]
	}
}
```


### Misono Branches
- 0: Misono "Eleison", comparable to Flashcord SID. Eleison is the unstable, very frequently updated version of Misono
- 1: Misono Stable