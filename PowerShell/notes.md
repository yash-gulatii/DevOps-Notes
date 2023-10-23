# PowerShell

## Resources Links

- [Microsoft Documentation](https://learn.microsoft.com/en-us/powershell/scripting/overview?view=powershell-7.3)

- [Youtube Video](https://www.youtube.com/watch?v=ZOoCaWyifmI&list=PLg9AuXJCWXi9R4Sh6KLHU5jz-ZauqH604&index=1&t=29s)


## Overview
PowerShell is a cross-platform task automation solution made up of a command-line shell, a scripting language, and a configuration management framework. PowerShell runs on Windows, Linux, and macOS.


#### Command-line Shell

PowerShell is a modern command shell that includes the best features of other popular shells. Unlike most shells that only accept and return text, PowerShell accepts and returns .NET Objects. The shell includes the followinf features:


- Robust command-line history
- Tab completion and command prediction
- Supports command and parameter aliases
- In-console help system, similar to Unix `man` pages

#### Scripting Language

As a scripting language, PowerShell is commonly used for autmating the management of systems. It's also used to build, test, and deploy soltuions, often in CI/CD enviornments. PowerShell is built on the .NET Comman Language Runtime (CLR). All inputs and outputs are .NET objects. o eed to parse text output to extract information from the output. The PowerShell scripting language includes the following features:


- Extensible through functions, classes, scripts, and modules
- Extensible formatting system for easy output
- Extensible type system for creating dynamic types
- Built-in support for common data formats like CSV, JSON, and XML

#### Automation platform

The extensible nature of PowerShell has enabled an ecosystem of PowerShell modules to deploy and manage almost any technology you work with. For example:


Microsoft :

- Azure
- Windows
- Exchange
- SQL

Third-Party :

- AWS
- VMWare
- Google Cloud

#### Configuration management

PowerShell Desired State Configuration (DSC) is a management framework inn PowerShell that enables you to manage your enterprise infrastructure with cofiguration as code. With DSC, you can:

- Create declarative configurations and custom scripts for repeatable deployments
- Enforce configuration settings and report on confirhuration drift
- Deploy configuration using push or pull models

### First Script

```pwsh
# My First Comment!!!
Write-Host "Hello world!"
```

### Some Commands

- Get-Command

```pwsh Get-Command -CommandTyper cmdlet```

- Get-Help

```pwsh Get-Help *(Any-Command)```

>Note- Asterisk`*` is used to display all the possible commands.

- Piping

Syntax:

```pwsh Command-1 | Command-2```

Example:

```pwsh "Hello World!!" | Out-File Helloworld.txt```

### Variables

A variable is a unit of memory in which values are stored. In PowerShell, variable are represented by the text strings that begin with a dollar sing($), such as $a, $process, or $my_var. Variable nnames aren't case-sensitive, and can include spaces and special characters.

#### Variable DataTypes

- Integers
- Floating Point Values
- Strings
- Booleans
- Datetime Values
