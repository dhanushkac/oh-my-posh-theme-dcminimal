# oh-my-posh theme - dcminimal
A customized PowerShell theme to use with oh-my-posh theme engine 👾

Follow [this guidelines](https://github.com/JanDeDobbeleer/oh-my-posh) to install the theme engine with your PowerShell instance.

You can create this `dcminimal.psm1` file in any name you need. That name will be considered as the theme name.

## Configuration

List the current configuration:

    $ThemeSettings

Copy this theme file into the location of `CurrentThemeLocation`.

Then, execute below.

    notepad $PROFILE

Your file would be similar to this after successfull installation.

    Import-Module posh-git
    Import-Module oh-my-posh
    Set-Theme Paradox

Update last line with your theme name. In my case it is as follows.

    Set-Theme dcminimal

I also updated the username shows in the terminal. Following code segment needs to be changed.

    if (Test-NotDefaultUser($user)) {
        $prompt += Write-Prompt -Object "$user@$computer " -ForegroundColor $sl.Colors.SessionInfoForegroundColor -BackgroundColor $sl.Colors.SessionInfoBackgroundColor
    }

Changed code segment as follows.

    if (Test-NotDefaultUser($user)) {
        $prompt += Write-Prompt -Object "Dhanushka@Terminal " -ForegroundColor $sl.Colors.SessionInfoForegroundColor -BackgroundColor $sl.Colors.SessionInfoBackgroundColor
    }

## Result

#### When there is no local changes

![No local changes](https://github.com/dhanushkac/oh-my-posh-theme-dcminimal/blob/main/images/no-local-changes.png)

#### When there are uncommited files

![Uncommitted changes](https://github.com/dhanushkac/oh-my-posh-theme-dcminimal/blob/main/images/local-changes.png)

#### When there are committed changes

![Committed changes](https://github.com/dhanushkac/oh-my-posh-theme-dcminimal/blob/main/images/ready-to-push.png)

