# NeovimConfiguration
***
## Prerequisitos
#### Plug:
```
curl -fLo ~/.local/share/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```
#### Gestor de autocompletado para Python:
```
pip3 install jedi
```
#### Gestor de autocompletado para c/c++:
```
sudo apt install ccls
```
#### npm para instalar extensiones de Coc:
```
sudo apt install npm
``` 
***
## Instalacion y Configuracion Extensiones
Copiar dentro del archivo de configuracion de plug las extensiones
```
Plug 'neoclide/coc.nvim', {'branch': 'release'}
Plug 'morhetz/gruvbox'
```
Posteriormente correr el comando de instalacion dentro de neo vim
```
:PlugInstall
```
Por ultimo copiar y pegar la carpeta de plug-config dentro del directorio de neo vim.

#### Configuracion Coc
Instalar todas las extensiones necesarias corriendo el comando de instalacion de Coc dentro de neo vim:
```
:CocInstall nombre-extension
```
Las extensiones que se usan en esta configuracion son:
* coc-explorer         
* coc-highlight       
* coc-html                 
* coc-snippets          
* coc-cmake                
* coc-css                    
* coc-json                  
* coc-python             
* coc-sql                    
* coc-yaml

###### Instalacion ccls y Configuracion del Explorador
Crear el archivo de configuracion coc-settings.json y dentro de el copiar la siguiente configuracion:
```
{
    "languageserver": {
        "ccls":{
            "command": "ccls",
            "filetypes": ["c", "cc", "cpp", "c++", "objc", "objcpp"],
            "rootPatterns": [".ccls", "compile_commands.json", ".git/", ".hg/"],
            "initializationOptions": {
                "cache":{
                    "directory": "/tmp/ccls"
                }
            }
        }
    },
    "explorer.width": 30,
    "explorer.icon.enableNerdfont": true,
    "explorer.previewAction.onHover": "labeling",
    "explorer.keyMappings.global": {
        "<cr>": ["expandable?", "expand", "open"],
        "v": "open:vsplit"
    }
}
```
Si no se instala la extension de coc-explorer ignorar las configuraciones de explorer.


