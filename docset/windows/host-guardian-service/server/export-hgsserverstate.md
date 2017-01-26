---
author: brianlic-msft
description: 
external help file: HgsServer-help.xml
keywords: powershell, cmdlet
manager: alanth
ms.date: 2016-12-20
ms.prod: powershell
ms.technology: powershell
ms.topic: reference
online version: 
schema: 2.0.0
title: Export-HgsServerState
ms.assetid: 4663C8BC-97CD-43C4-A43F-3EFBA479A710
---

# Export-HgsServerState

## SYNOPSIS
Exports the local Host Guardian Service instance's state to enable recovery scenarios.

## SYNTAX

```
Export-HgsServerState [[-Path] <String>] -Password <SecureString> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Export-HgsServer** cmdlet exports the Host Guardian Service (HGS) state to enable recovery scenarios.

The cmdlet causes the following Host Guardian Service state to be exported to the specified output file: 

- Attestation Service policies
- Attestation Service configuration data
- Key Protection policies
- Key Protection configuration data
- Key Protection Signer Certificates and private keys
- Key Protection Encryption Certificates and private keys

For more information about the scenario terms, see Security and Assurancehttp://go.microsoft.com/fwlink/?LinkId=699209 (http://go.microsoft.com/fwlink/?LinkId=699209).

## EXAMPLES

### Example 1: Export HGS server state and protect it with a password
```
PS C:\>Export-HgsServerState -Path "C:\HGS\ExportState.xml" -Password $Pass
Encrypted HGS Server State stored at the specified location
```

This command exports the HGS server state and protects the exported state using a password.
The exported state is stored at the file specified by the **Path** parameter.

Use the ConvertTo-SecureString cmdlet to generate a secure string that represents the password.

## PARAMETERS

### -Path
Specifies the path for the exported file.

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
Specifies the password with which to encrypt the keys.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[HGS Server Cmdlets](./index.md)
