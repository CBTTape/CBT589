# CBT589
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 589 is from Philippe Leite and contains a REXX function   *   FILE 589
//*           package to handle STK silo commands.  The package is  *   FILE 589
//*           called HSCTOOL.  Also added to this file is a TSO     *   FILE 589
//*           command to issue Hercules commands if MVS is running  *   FILE 589
//*           under Hercules.  The command is called HERCMD.        *   FILE 589
//*                                                                 *   FILE 589
//*    email:  Philippe Leite <pbleite@br.ibm.com>                  *   FILE 589
//*                                                                 *   FILE 589
//*    Program:       HSCTOOL                                       *   FILE 589
//*    Author:        PHILIPPE LEITE                                *   FILE 589
//*    Objective:     HSC (STORAGETEK) - REXX EXTERNAL FUNCTION     *   FILE 589
//*    Creation Date: 26/05/2004                                    *   FILE 589
//*                                                                 *   FILE 589
//*                   H S C T O O L   Version 1.1.5                 *   FILE 589
//*                                                                 *   FILE 589
//*       HSCTOOL is an REXX external function that works as        *   FILE 589
//*       an interface between a REXX Exec and HSC (StorageTek      *   FILE 589
//*       Robots). The following features are implemented in        *   FILE 589
//*       the HSCTOOL:                                              *   FILE 589
//*                                                                 *   FILE 589
//*       EJECT    - Eject volume from an ACS.                      *   FILE 589
//*       MOUNT    - Mount volume.                                  *   FILE 589
//*       DISMOUNT - Dismount volume.                               *   FILE 589
//*       MOVE     - Move a Volume to another LSM.                  *   FILE 589
//*       QCAP     - Query capacity and status of a CAP.            *   FILE 589
//*       QCONFIG  - Get configuration data.                        *   FILE 589
//*       QHSC     - Determine HSC status.                          *   FILE 589
//*       QDSN     - Get Data set information.                      *   FILE 589
//*       QDRIVES  - Get Drive information.                         *   FILE 589
//*       QSCRATCH - Get LSM scratch counts.                        *   FILE 589
//*       QVOLUME  - Get volume status.                             *   FILE 589
//*       SCRATCH  - Return a volume to scratch status.             *   FILE 589
//*       UNSCRATCH - Remove a volume from scratch status.          *   FILE 589
//*                                                                 *   FILE 589
//*      Illustration of one function:  see member $$$$DOC for      *   FILE 589
//*      complete details for all functions:                        *   FILE 589
//*                                                                 *   FILE 589
//*      EJECT function:                                            *   FILE 589
//*      ==============                                             *   FILE 589
//*                                                                 *   FILE 589
//*      SYNTAX:   HSCTOOL('EJECT','Volume')                        *   FILE 589
//*                                                                 *   FILE 589
//*      Variables returned:                                        *   FILE 589
//*                                                                 *   FILE 589
//*         RESULT    - Return Code                                 *   FILE 589
//*         @SLXCMDRC - Return Code (in hex)                        *   FILE 589
//*         @SLXSRC   - Reason Code (HSC Message Code in hex)       *   FILE 589
//*                                                                 *   FILE 589
//*      Possible Return Codes:                                     *   FILE 589
//*                                                                 *   FILE 589
//*         00  -  Successful operation.                            *   FILE 589
//*         08  -  Invalid Parm specified.                          *   FILE 589
//*         16  -  Operation failed. Look at @SLXSRC for the        *   FILE 589
//*                reason rode                                      *   FILE 589
//*         20  -  HSC is not available.                            *   FILE 589
//*         24  -  User not Authorized. The request was failed      *   FILE 589
//*                by Exit SLSUX05 or the HSC Default               *   FILE 589
//*                authorization.                                   *   FILE 589
//*         50  -  Invalid Return Code by SLSXCAL.                  *   FILE 589
//*         60  -  Error in SET Varibles CSECT.                     *   FILE 589
//*                                                                 *   FILE 589
//*      Example:                                                   *   FILE 589
//*                                                                 *   FILE 589
//*      /* rexx */                                                 *   FILE 589
//*                                                                 *   FILE 589
//*      result = HSCTOOL('EJECT','011000')                         *   FILE 589
//*      if result = 0 then say "Eject successful"                  *   FILE 589
//*                                                                 *   FILE 589
//*      -------------------------------------------------------    *   FILE 589
//*                                                                 *   FILE 589
//*      Description of HERCMD.                                     *   FILE 589
//*                                                                 *   FILE 589
//*         TSO command processor to issue Hercules commands        *   FILE 589
//*         through Diagnose instruction (function code x'008')     *   FILE 589
//*         and display response from Hercules virtual machine.     *   FILE 589
//*         The Hercules parameter diag8cmd must be enabled.        *   FILE 589
//*                                                                 *   FILE 589
//*      Example:  TSO HERCMD ATTACH 0A90 3390 disk.0a90            *   FILE 589
//*                                                                 *   FILE 589
```
