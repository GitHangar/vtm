# VTM

A text-based desktop environment in your terminal
![image](https://dice.netxs.online/cloud/vtm/mde_banner_v1.11.png)

# Demo

- Live SSH Demo

  `ssh vtm@netxs.online`

- Video
  - [Desktop environment](https://youtu.be/fLumnSctakY)
  - [Collaborative interaction](https://youtu.be/0zU4e5Vam8c)
  - [Recursive connection](https://youtu.be/Fm5X75sO62c)

# Supported Platforms

- GNU/Linux amd64
- Windows
  - Windows 10 (32/64)
  - Windows Server 2019 (32/64)
- macOS
  - Catalina 10.15

# Releases

[![](https://dice.netxs.online/cloud/vtm/status/macos)](https://github.com/netxs-group/VTM/releases/download/latest/vtm_macos.tar.gz)  
[![](https://dice.netxs.online/cloud/vtm/status/linux)](https://github.com/netxs-group/VTM/releases/download/latest/vtm_linux_amd64.tar.gz)  
[![](https://dice.netxs.online/cloud/vtm/status/windows)](https://github.com/netxs-group/VTM/releases/download/latest/vtm_windows_64.zip)  

---

# Command Line Options

Module               | Options
---------------------|--------------------------------------
`vtm(.exe)` client   | No arguments
`vtmd(.exe)` server  | `[ -d ]` run in background

# User Interface Commands

`ButtonClick + Drag` = `ButtonDrag`

Shortcut              | Action
----------------------|--------------------------------------
`Ctrl + PgUp/Dn`      | Switch between windows
`LeftClick`           | Assign exclusive keyboard focus
`Ctrl + LeftClick`    | Assign/clear group keyboard focus
double `LeftClick`    | Window: Maximize/restore
`RightClick`          | Desktop: Call menu
`Left + Right`<br>or `MiddleClick` | Window: Close/destroy
`LeftDrag`            | Desktop: Move visible windows<br>Window: Resize/move
`RightDrag`           | Desktop: Create new window<br>Window: Scroll content
`Left + RightDrag`    | Scroll workspace
`Ctrl + RightDrag`<br>or `Ctrl + MiddleDrag` | Copy selected area to clipboard `OSC 52`

# Built-in Applications

- `▀▄ Term` Terminal emulator
- `▀▄ Logs` VT monitoring tool
- `▀▄ Task` Task manager (desktopio) _(not ready)_
- `▀▄ Hood` Configuration utility _(not ready)_
- `▀▄ Info` Documentation browser _(not ready)_
- `▀▄ Shop` TUIs distribution platform _(not ready)_
- `▀▄ Text` ANSI/VT Text editor _(not ready)_
- `▀▄ Calc` Spreadsheet calculator _(not ready)_
- `▀▄ Draw` ANSI-artwork editor _(not ready)_
- `▀▄ File` File manager _(not ready)_
- `▀▄ Goto` Internet/SSH browser _(not ready)_
- `▀▄ Clip` Clipboard manager _(not ready)_
- `▀▄ Char` Unicode codepoints browser _(not ready)_
- `▀▄ Time` Calendar application _(not ready)_
- `▀▄ Doom` Doom Ⅱ source port _(not ready)_

<details><summary>show details...</summary><p>

 - `▀▄ Term`
   - UTF-8 Everywhere
   - Unicode clustering
   - TrueColor/256-color support
   - Auto-wrap mode `DECAWM` (with horizontal scrolling)
   - Focus tracking `DECSET 1004`
   - Bracketed paste mode `DECSET 2004`
   - SGR attributes: overline, double underline, strikethrough, and others
   - Save/restore terminal window title `XTWINOPS 22/23`
   - Mouse tracking `DECSET 1000/1002/1003/1006 SGR` mode
   - Mouse tracking `DECSET 10060 Extended SGR` mode, mouse reporting outside of the terminal viewport (outside + negative arguments) #62
   - Configurable using VT-sequences
   
      Name         | Sequence                         | Description
      -------------|----------------------------------|-------------
      `CCC_SBS`    | `CSI` 24 \[ : n \[ : m \] \] `p` | Set scrollback buffer size, `int32_t`<br>`n` Buffer limit in lines, 0 is unlimited, _default is 20.000_<br>`m` Grow step for unlimited buffer, _default is 0_
      `CCC_RST`    | `CSI`  1           `p`           | Reset all parameters to default
      `CCC_TBS`    | `CSI`  5 \[ : n \] `p`           | Set tabulation length<br>`n` Length in chars, _max = 256, default is 8_
      `CCC_JET`    | `CSI` 11 \[ : n \] `p`           | Set text alignment, _default is Left_<br>`n = 0` default<br>`n = 1` Left<br>`n = 2` Right<br>`n = 3` Center
      `CCC_WRP`    | `CSI` 12 \[ : n \] `p`           | Set text autowrap mode, _default is On_<br>`n = 0` default<br>`n = 1` On<br>`n = 2` Off
      `CCC_RTL`    | `CSI` 13 \[ : n \] `p`           | Set text right-to-left mode, _default is Off_<br>`n = 0` default<br>`n = 1` On<br>`n = 2` Off

 - `▀▄ Logs`
  - Reset by double `RightClick`

 - `▀▄ Hood`
  - ...

 - `▀▄ Info`
  - ...

 - `▀▄ Shop`
  - Just a sketch

 - `▀▄ Text`
  - A user interface only

 - `▀▄ Calc`
  - A user interface only

 - `▀▄ Clip`
  - ...

 - `▀▄ Draw`
  - ...

 - `▀▄ Task`
  - ...

 - `▀▄ Char`
  - ...

 - `▀▄ File`
  - ...

 - `▀▄ Time`
  - ...

 - `▀▄ Goto`
  - ...

 - `▀▄ Doom`
  - ...

</p></details>

# Related Repositories

[Desktopio Framework Documentation](https://github.com/netxs-group/Desktopio-Docs)

---

[![HitCount](https://views.whatilearened.today/views/github/netxs-group/VTM.svg)](https://github.com/netxs-group/VTM) [![Gitter](https://badges.gitter.im/netxs-group/VTM.svg)](https://gitter.im/netxs-group/VTM?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge) [![Twitter handle][]][twitter badge]

[//]: # (LINKS)
[twitter handle]: https://img.shields.io/twitter/follow/desktopio.svg?style=social&label=Follow
[twitter badge]: https://twitter.com/desktopio
