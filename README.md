
- [Objetivos](#objetivos)
- [Preparando zsh](#preparando-zsh)
  * [Instalando zsh](#instalando-zsh)
  * [Instalando o Oh-My-ZSH](#instalando-o-oh-my-zsh)
  * [Instalando plugins](#instalando-plugins)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

# Objetivos

Esse repositorio tende a facilitar minha vida com o start de configurações para conseguir trabalhar


# Preparando zsh

zsh é igual bash ou o proprio sh mas tem uns plugins que ajudam.

# Instalando zsh

Observações:
- O mac não precisa instalar.
- No windows tu tem que instalar no WSL (Windows Subsystem Linux)

```sh
sudo apt install zsh -y
```

# Instalando o Oh-My-ZSH

Essa é a extensão que deixa as paradas bonias.
O link para a pagina de instalação é esse: https://ohmyz.sh/#install

Comando direto porque sou preguiçoso

```sh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

# Instalando plugins

## Systax Highlight

O link desse puglin é esse: [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)

Codigo para preguiçoso.

**OBS: pode estar desatualizado**

1. Clone this repository in oh-my-zsh's plugins directory:

    ```zsh
    git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
    ```

2. Activate the plugin in `~/.zshrc`:

    ```zsh
    plugins=( [plugins...] zsh-syntax-highlighting)
    ```

3. Restart zsh (such as by opening a new instance of your terminal emulator).


## Auto Suggestions

O link desse puglin é esse: [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md)

Codigo para preguiçoso.

**OBS: pode estar desatualizado**

1. Clone this repository into `$ZSH_CUSTOM/plugins` (by default `~/.oh-my-zsh/custom/plugins`)

    ```sh
    git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
    ```

2. Add the plugin to the list of plugins for Oh My Zsh to load (inside `~/.zshrc`):

    ```sh
    plugins=( 
        # other plugins...
        zsh-autosuggestions
    )
    ```

3. Start a new terminal session.

## Thema

Tem um tema que eu não gosto muito mas a documentação dele é boa. Chama SpaceshipZSH ele é bem pesado por isso eu não gosto muito. O link dele é o seguinte: [spaceship-promp](https://github.com/spaceship-prompt/spaceship-prompt)

Os comandos para aderir qualquer tema é esse:

- Clone this repo (aqui é so colocar o arquivo do seu thema na pasta correta ):

```zsh
# Exemplo
git clone https://github.com/arquivo_thema_x "$ZSH_CUSTOM/themes/thema_x" --depth=1

# Exemplo concreto
git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
```

- Symlink `spaceship.zsh-theme` to your oh-my-zsh custom themes directory:

```zsh
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```

- Set `ZSH_THEME="spaceship"` in your `.zshrc`.

Atualmente estou usando um tema padrão que é o `ZSH_THEME="gnzh"`

4. Plugin de gestão de comandos antigos

```zsh
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```
