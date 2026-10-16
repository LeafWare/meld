### [Meld](https://meldmerge.org)

#### Install using Git

If you are a Git user, you can install the theme and keep it up to date by cloning the repo:

```bash
git clone https://github.com/dracula/meld.git
```

#### Install manually

Download using the [GitHub `.zip` download](https://github.com/dracula/meld/archive/main.zip) option and unzip it.

#### Activating theme

Meld reads GtkSourceView 4 style schemes from a `gtksourceview-4/styles` folder in its data directory. Copy `dracula.xml` there:

**Linux**

```bash
mkdir -p ~/.local/share/gtksourceview-4/styles
cp dracula.xml ~/.local/share/gtksourceview-4/styles/
```

**macOS** (the [Meld for macOS](https://gitlab.com/dehesselle/meld_macos) build, also available as the Homebrew cask `meld`)

```bash
mkdir -p ~/Library/Application\ Support/org.gnome.Meld/share/gtksourceview-4/styles
cp dracula.xml ~/Library/Application\ Support/org.gnome.Meld/share/gtksourceview-4/styles/
```

**Windows**

Copy `dracula.xml` to `%LOCALAPPDATA%\gtksourceview-4\styles\` (create the folders if they do not exist).

Then:

1. Restart Meld;
2. Open Preferences, Editor tab, and pick **Dracula** under _Syntax highlighting color scheme_;
3. Boom! It's working ✨

To set it from the command line instead, on Linux run `gsettings set org.gnome.meld style-scheme dracula` and on macOS run `defaults write org.gnome.Meld "/org/gnome/meld/style-scheme" dracula`.
