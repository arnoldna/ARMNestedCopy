# ARM Nested Copy with Zero Based Array

This code demonstrates how a zero length array errors when passing to a copy function in a linked template.

## Environment Setup

---

* Create an resource group called `test-rg`
* Change the `adminUsername` and `adminPassword` in the following parameters.json files
  * vm-datadisk.parameters.json
  * vm-no-datadisk.parameters.json

## Scenario

Run the VM creation with no data disks.

### VM Creation with No Data Disks

```powershell
New-AzResourceGroupDeployment -ResourceGroupName test-rg -TemplateParameterFile '.\vm-no-datadisk.parameters.json'  -TemplateUri 'https://raw.githubusercontent.com/arnoldna/ARMNestedCopy/master/WindowsLinkedDeployments/vm.nested.deploy.json' -debug
```

### Working Zero Length Copy

```powershell
New-AzResourceGroupDeployment -ResourceGroupName test-rg -TemplateParameterFile '.\vm-datadisk.parameters.json'  -TemplateUri 'https://raw.githubusercontent.com/arnoldna/ARMNestedCopy/master/WindowsLinkedDeployments/vm.nested.deploy.json' -debug
```