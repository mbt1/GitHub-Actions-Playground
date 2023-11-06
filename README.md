# GitHub-Actions-Playground

## Variables from step to step within the same job

### Setting a variable
#### In PowerShell:
`echo "some_other_var=some value" | Out-File -Append -FilePath $env:GITHUB_ENV`
Make sure there is **no space** around the equal sign as it would become part of either the value or the name!

### Reading a variable
#### In Powershell
`Write-Host "some_other_var = $env:some_other_var";`

#### In the shell
`echo $some_other_var`

#### In an Action Step that is not a shell
`${{ env.some_other_var }}`
