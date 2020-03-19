# ARMNestedCopy

## Working Zero Length Copy

```powershell
New-AzResourceGroupDeployment -ResourceGroupName nate-test-rg -TemplateParameterFile vm-no-datadisk.parameters.json -TemplateFile .\vm.deploy.json
```