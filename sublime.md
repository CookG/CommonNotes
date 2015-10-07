# Install Sublime After installation, just connect sublime with command line by

`ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/sublime`

## Get Package Control
Go to **View > Show Console**, and paste
`import urllib.request,os,hashlib; h = '2915d1851351e5ee549c20394736b442' + '8bc59f460fa1548d1514676163dafc88'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)`

## Install Material Theme
Go to Package Control, install Material Theme
In the User Setting
`"theme": "Material-Theme.sublime-theme",
 "color_scheme": "Packages/Material Theme/schemes/Material-Theme.tmTheme",`

` "overlay_scroll_bars": "enabled",
  "font_face": "Monaco for Powerline",
  "font_size": 18,
  "bold_folder_labels": true,
  "indent_guide_options": [ "draw_normal", "draw_active" ],
`

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
