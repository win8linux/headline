# Headline ZSH Theme
![Screenshot_20240319_105537](https://github.com/win8linux/headline/assets/11584387/af1ece62-70e5-419a-b251-b1a0fc6d8535)


Headline. A stylish theme with deliberate use of space. No dependencies. Customizable.

<br>


## Features
### Separator Line
A line above the prompt info text with matching colors. May be disabled with `HEADLINE_LINE_MODE=off` for a more compact prompt.

### Information Line
`<user> @ <host>: <path> | <branch> [<status>]`

This line collapses to fit within the terminal width. Individually style each segment of the information line using [ANSI SGR codes](https://en.wikipedia.org/wiki/ANSI_escape_code#SGR_(Select_Graphic_Rendition)_parameters) (which are conveniently aliased in the theme file). You can customize the characters for joining segments and disable segments entirely.

### Git Status
All the Git status symbols are customizable. The defaults are below:

| Symbol | Meaning          |
|--------|------------------|
| `+`    | staged changes   |
| `!`    | unstaged changes |
| `?`    | untracked files  |
| `↓`    | commits behind   |
| `↑`    | commits ahead    |
| `↕`    | commits diverged |
| `*`    | stashed files    |
| `✘`    | conflicts        |
| (none) | clean branch     |

### *Exit Code*
`→ <code> (<meaning>)`

When enabled with `HEADLINE_DO_ERR=true`, print non-zero exit codes ahead of the prompt. The exit code meaning is merely a guess for the semi-standard exit codes (in the range 126-143) and is often incorrect.

### *Clock*
When enabled with `HEADLINE_DO_CLOCK=true`, display the time to the right of the prompt.

<br>


## Installation
Download the `headline.zsh-theme` file.
```
$ wget https://raw.githubusercontent.com/win8linux/headline/main/headline.zsh-theme
```

In your `~/.zshrc`, source the `headline.zsh-theme` file.
```
source your/path/to/headline.zsh-theme
```

More details in **[Installation](docs/Installation.md)**

<br>


## Customization
<img src="https://raw.githubusercontent.com/moarram/headline/assets/images/configs.gif" width="600"/>

The `headline.zsh-theme` file describes variables ([around line 70](headline.zsh-theme#L70)) for customizing prompt behavior, colors, styles, symbols, etc. You can edit the theme file directly or set these variables in your `~/.zshrc` *after* sourcing the theme to override the defaults. Play around with it and make it your own!

More details in **[Customization](docs/Customization.md)**

<br>


## Terminal Setup
For the continuous line above the prompt, no further setup is needed! Use any font you want, as long as it has the ▁ (Lower One-eighth Block) symbol.

If you want symbols, use a font that has them such as [FiraCode Nerd Font](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraCode) and assign your desired symbols to the prefix variables.

More details in **[Terminal Setup](docs/Terminal-Setup.md)**

<br>


## Screenshots
Screenshots of theme in [iTerm2](https://iterm2.com/index.html). Using [FiraCode Nerd Font](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraCode) for continuous line and fancy icons.

**NOTE:** A font with ligatures is no longer required for a continuous line.

> <img src="https://raw.githubusercontent.com/moarram/headline/assets/images/theme-light.png" width="600"/>
>
> Status showing `+` for staged changes, `!` for unstaged changes, and `?` for untracked files (configurable).

> <img src="https://raw.githubusercontent.com/moarram/headline/assets/images/theme-brown.png" width="600"/>
>
> Optional icons, special font needed.

> <img src="https://raw.githubusercontent.com/moarram/headline/assets/images/theme-dark.png" width="600"/>
>
> Path truncated to fit in available space, user and host hidden.

> <img src="https://raw.githubusercontent.com/moarram/headline/assets/images/feature-clock-and-exit-code.png" width="600"/>
>
> Optionally show clock and exit code.

Screenshots of updated theme in [Konsole](https://apps.kde.org/konsole) using [IBM Plex Mono](https://www.ibm.com/plex/) and [BlexMono](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/IBMPlexMono) for icons.

> ![Screenshot_20240319_101937](https://github.com/win8linux/headline/assets/11584387/8088f029-06ce-4c23-9075-7fd5c18099ae)
>
> Status showing `+` for staged changes, `!` for unstaged changes, and `↑` for untracked files (configurable).

> ![Screenshot_20240319_104232](https://github.com/win8linux/headline/assets/11584387/25350ac1-b150-4cdd-8b44-3b236194a966)
>
> Optional icons, special font needed (such as BlexMono here).

<br>


## Related
* [Headline Oh My Posh Theme](https://github.com/wathhr/headline-omp)

<br>


## Credits
* Headline's Git status functions are inspired by `git.zsh` in [Oh-My-Zsh's core library](https://github.com/ohmyzsh/ohmyzsh/blob/master/lib).
* Thanks to u/romkatv (author of [Powerlevel10k](https://github.com/romkatv/powerlevel10k)) for the [Reddit post](https://old.reddit.com/r/zsh/comments/cgbm24/multiline_prompt_the_missing_ingredient/) describing how to calculate prompt string display length.
