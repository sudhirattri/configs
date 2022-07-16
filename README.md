# configs

### Linux Shell Commands (bash, zsh, . . . )

- Windows directory colors -

  - `export LS_COLORS="$LS_COLORS:ow=1;34:tw=1;34:"`
- Code OSS extensionsGallery fix -

  - sudo nano /lib/code/product.json

  ```
    "extensionsGallery": {
            "serviceUrl": "https://marketplace.visualstudio.com/_apis/public/gallery",
        "cacheUrl": "https://vscode.blob.core.windows.net/gallery/index",
        "itemUrl": "https://marketplace.visualstudio.com/items"
      }
  ```
- SSH migration (for github)

  - Copy ~/.ssh
  - Change permissions - `chmod 600 ~/.ssh/idXXXXX`

### i3 Config for shortcuts and window filters (full config in ./config-i3)

- Brightness (software brightness)

  - xrandr --output DP-4 --brightness 0.6
- Mouse Flat acceleration profile

  - xinput --set-prop id 'libinput Accel Profile Enabled' 0, 1
- Wifi Connect

  - nmcli device wifi connect "ssid" password "pass"

### Arch install and maintainence (using archfi)

- rfkill unblock all
- iwctl
- station wlan0 connect "ssid"
- curl -L archfi.sf.net/archfi > archfi
- sh archfi
- chroot -
  - mount /dev/sdax /mnt
  - arch-chroot /mnt
- Install base-devel package to install sudo and later access sudo settings.
- Install must - network manager, xorg, graphic driver, os-prober (for dual boot)

### VScode settings

```
{
    "workbench.colorTheme": "Monokai Pro (Filter Octagon)",
    "workbench.iconTheme": "Monokai Pro (Filter Octagon) Icons",
    "editor.fontFamily": "JetBrains Mono",
    "terminal.integrated.fontWeight": "900",
    "terminal.integrated.fontFamily": "JetBrains Mono",
    "terminal.integrated.fontSize": 16,
    "editor.fontSize": 16,
    "editor.fontWeight": "800",
    // "editor.lineHeight": 24,
    "explorer.decorations.colors": false,
    "explorer.decorations.badges": false,
    "window.menuBarVisibility": "toggle",
    "editor.find.addExtraSpaceOnTop": false,
    "editor.cursorBlinking": "smooth",
    "editor.cursorWidth": 2,
    "editor.formatOnSave": true,
    "workbench.colorCustomizations": {
        "sideBar.foreground": "#eee",
        "gitDecoration.modifiedResourceForeground": "#7cf"
    },
    // "editor.codeActionsOnSave": {
    //     "source.fixAll.eslint": true,
    // },
    // "eslint.validate": [
    //     "javascript"
    // ],
    "material-icon-theme.folders.theme": "classic",
    "material-icon-theme.folders.color": "#fdd835",
    "files.exclude": {
        "**/.classpath": true,
        "**/.project": true,
        "**/.settings": true,
        "**/.factorypath": true
    },
    "editor.inlineSuggest.enabled": true,
    "terminal.integrated.enableMultiLinePasteWarning": false
}
```

### Alacritty Config

```
shell:
  program: wsl
  args:
    - --cd /home/sudhir/studio

window:
  dimensions:
    columns: 120
    lines: 24
  opacity: 0.9

font:
  normal:
    family: JetBrains Mono
    style: Medium

  bold:
    family: JetBrains Mono
    style: Bold

  italic:
    family: JetBrains Mono
    style: Italic

  bold_italic:
    family: JetBrains Mono
    style: Bold Italic
  size: 14.0

key_bindings:
    # (Windows, Linux, and BSD only)
  - { key: V,         mods: Control|Shift, action: Paste                       }
  - { key: C,         mods: Control|Shift, action: Copy                        }
  - { key: Key0,      mods: Control,       action: ResetFontSize               }
  - { key: Equals,    mods: Control,       action: IncreaseFontSize            }
  - { key: Plus,      mods: Control,       action: IncreaseFontSize            }
  - { key: Minus,     mods: Control,       action: DecreaseFontSize            }
  - { key: F11,       mods: None,          action: ToggleFullscreen            }
  - { key: L,         mods: Control,       action: ClearLogNotice              }
  - { key: L,         mods: Control,       chars: "\x0c"                       }
  - { key: K,         mods: Control,       action: ClearHistory                }
  - { key: PageUp,    mods: None,          action: ScrollPageUp,   mode: ~Alt  }
  - { key: PageDown,  mods: None,          action: ScrollPageDown, mode: ~Alt  }
  - { key: Home,      mods: Shift,         action: ScrollToTop,    mode: ~Alt  }
  - { key: End,       mods: Shift,         action: ScrollToBottom, mode: ~Alt  }
```

### Bashcrc and other dotfiles
