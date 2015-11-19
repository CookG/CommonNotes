# Install Sublime After installation, just connect sublime with command line by
```
ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/sublime
```
## Get Package Control
Go to **View > Show Console**, and paste
```
import urllib.request,os,hashlib; h = '2915d1851351e5ee549c20394736b442' + '8bc59f460fa1548d1514676163dafc88'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

## Install Material Theme
Go to Package Control, install Material Theme
In the User Setting
```
{
  	"theme": "Material-Theme.sublime-theme",
	"color_scheme": "Packages/Material Theme/schemes/Material-Theme.tmTheme",
	"ignored_packages":
	[
		"Vintage"
	],

  	"overlay_scroll_bars": "enabled",
  	"bold_folder_labels": true,
  	"indent_guide_options": [ "draw_normal", "draw_active" ],    // Highlight active indent
  	"font_options": [ "Monaco for Powerline Regular" ],
  	"font_face": "Monaco for Powerline",
  	"font_size": 12,
  	"material_theme_small_tab": false,                          // Set small tabs
 	"material_theme_disable_fileicons": false,                  // Hide siderbar file type icons
  	"material_theme_disable_folder_animation": false,           // Disable folder animation
  	"material_theme_small_statusbar": false,                    // Set small status bar
  	"material_theme_disable_tree_indicator": false,             // Disable sidebar file indicator
  	"material_theme_bold_tab": false,                           // Make the tab labels bolder
  	"material_theme_tabs_separator": false,                     // Show tabs separator
  	"material_theme_accent_lime": true,                         // set green lime accent color
  	//"material_theme_accent_purple": true,                       // set purple accent color
  	//"material_theme_accent_red": true,                          // set pale red accent color
  	//"material_theme_accent_orange": true,                       // set orange accent color
  	//"material_theme_accent_yellow": true,                       // set yellow accent color
  	"material_theme_panel_separator": false,                     // show bottom panel separator
  	"material_theme_tabs_autowidth": false,                      // Enable autowidth for tabs
  	"material_theme_contrast_mode": false,                       // Enable sidebar and panels contrast mode
}
```

## Install Modelica mode
## Install VHDL mode
## Install Trimmer
Not sure how useful it will be though...

## Install MarkdownEditting and Markdown Preview
## Install LatexTools if it is needed.

## Remeber previous files
`"remember_open_files": true,
 "hot_exit": false,
 "tab_size": 4,
 "translate_tabs_to_spaces": true,
 "highlight_line": true,
 "highlight_modified_tabs": true,
`
## Install Terminal
`{
    "terminal": "iTerm.sh",
 }`

## Install SideBarEnhancements and FileDiffs

## Better style
`"draw_white_space": "all",
"rulers": [80, 100],
"trim_trailing_white_space_on_save": true,
"ensure_newline_at_eof_on_save": true,
`

## Install HTMLBeautify
## Install AutoPEP8
## Install Alignment
## Install AllAutocomplete
## Install Plaintasks
