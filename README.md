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


Es necesario instalar el gestor de paquetes Plug para Neovim, el gestor de
autocompletado para python jedi, y el gestor de autocompletado para c/c++ ccls. 
