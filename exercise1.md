The team develops the software using the dotnet stack and C# programming language. A tool for **linting** in dotnet is [dotnet-format](https://github.com/dotnet/format) which is a code style formatting tool for C#. Style format preferences for a C# project are defined in a `.editorconfig` file. A tool for **testing** is [xUnit](https://xunit.net/) which is an opensource unit testing tool. **Building** dotnet projects is done through the dotnet `build` command. This compiles project files to Integrated Language (IL) binaries. These binaries are interpreted by the Common Language Runtime (CLR) which then compiles these binaries to machine specific code (win, mac, …) and executes it.

Commands for all 3 activities are available in dotnet which can be used in a CI process:
* Linting: `dotnet format`
* Testing: `dotnet test`
* Building: `dotnet build`

A tool for CI in dotnet is Azure DevOps. Azure DevOps is a cloud-based solution to manage the full software development lifecycle. Besides CI, it also provides capabilities to manage and track projects, test applications, code repositories, etc.
CI can be configured in Azure DevOps through what is called pipelines. Pipelines (similar to workflows in Github Actions) are a collection of tasks (steps in Github actions) to perform CI tasks, such as building, testing, linting, etc. Tasks for the above mentioned tools are available in Azure DevOps.

Based on the available information, that the team consists of 6 members, a cloud-based solution would be a good choice as it is easy to setup and requires fewer maintenance. The team can therefore focus on other tasks. However, to make a better assessment, we need to look at whether the team is part of a bigger organisation, are there already existing CI tools in place, what about security requirements, etc.