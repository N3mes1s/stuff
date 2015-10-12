#[System Service Call Implementations in the WRK](http://www.dcl.hpi.uni-potsdam.de/research/WRK/2007/11/system-service-call-implementations-in-the-wrk/)

By Michael Schöbel

The kernel of a Windows Server 2003 Enterprise Edition system provides 296 system service calls. A complete list which allows comparison with Windows versions up to Windows Vista can be found [here](http://www.metasploit.com/users/opcode/syscalls.html).

Not all system service call implementations are contained in the Windows Research Kernel source code. The following table shows the available system service implementations (Nt*-functions) with reference to the corresponding source code file.

As the WRK readme.txt states …

> The kernel sources excluded from the kit are primarily in the areas of plug-and-play, power management, the device verifier, kernel debugger interface, and virtual dos machine.

… the most of the missing system service implementations are related to power management, plug-and-play, and device drivers.

* * *

<table>

<tbody>

<tr>

<th>Nr.</th>

<th>Function</th>

<th>File</th>

<th>Line</th>

</tr>

<tr>

<td> 0×0000 </td>

<td> NtAcceptConnectPort </td>

<td> base/ntos/lpc/lpccompl.c </td>

<td> 38 </td>

</tr>

<tr>

<td> 0×0001 </td>

<td> NtAccessCheck </td>

<td> base/ntos/se/accessck.c </td>

<td> 2370 </td>

</tr>

<tr>

<td> 0×0002 </td>

<td> NtAccessCheckAndAuditAlarm </td>

<td> base/ntos/se/seaudit.c </td>

<td> 1794 </td>

</tr>

<tr>

<td> 0×0003 </td>

<td> NtAccessCheckByType </td>

<td> base/ntos/se/accessck.c </td>

<td> 2458 </td>

</tr>

<tr>

<td> 0×0004 </td>

<td> NtAccessCheckByTypeAndAuditAlarm </td>

<td> base/ntos/se/seaudit.c </td>

<td> 1855 </td>

</tr>

<tr>

<td> 0×0005 </td>

<td> NtAccessCheckByTypeResultList </td>

<td> base/ntos/se/accessck.c </td>

<td> 2559 </td>

</tr>

<tr>

<td> 0×0006 </td>

<td> NtAccessCheckByTypeResultListAndAuditAlarm </td>

<td> base/ntos/se/seaudit.c </td>

<td> 1921 </td>

</tr>

<tr>

<td> 0×0007 </td>

<td> NtAccessCheckByTypeResultListAndAuditAlarmByHandle </td>

<td> base/ntos/se/seaudit.c </td>

<td> 1987 </td>

</tr>

<tr>

<td> 0×0008 </td>

<td> NtAddAtom </td>

<td> base/ntos/ex/exatom.c </td>

<td> 53 </td>

</tr>

<tr>

<td> 0×0009 </td>

<td> NtAddBootEntry </td>

</tr>

<tr>

<td> 0×000A </td>

<td> NtAddDriverEntry </td>

</tr>

<tr>

<td> 0×000B </td>

<td> NtAdjustGroupsToken </td>

<td> base/ntos/se/tokenadj.c </td>

<td> 435 </td>

</tr>

<tr>

<td> 0×000C </td>

<td> NtAdjustPrivilegesToken </td>

<td> base/ntos/se/tokenadj.c </td>

<td> 41 </td>

</tr>

<tr>

<td> 0×000D </td>

<td> NtAlertResumeThread </td>

<td> base/ntos/ps/psspnd.c </td>

<td> 534 </td>

</tr>

<tr>

<td> 0×000E </td>

<td> NtAlertThread </td>

<td> base/ntos/ps/psspnd.c </td>

<td> 483 </td>

</tr>

<tr>

<td> 0×000F </td>

<td> NtAllocateLocallyUniqueId </td>

<td> base/ntos/ex/luid.c </td>

<td> 67 </td>

</tr>

<tr>

<td> 0×0010 </td>

<td> NtAllocateUserPhysicalPages </td>

<td> base/ntos/mm/physical.c </td>

<td> 1415 </td>

</tr>

<tr>

<td> 0×0011 </td>

<td> NtAllocateUuids </td>

<td> base/ntos/ex/uuid.c </td>

<td> 628 </td>

</tr>

<tr>

<td> 0×0012 </td>

<td> NtAllocateVirtualMemory </td>

<td> base/ntos/mm/allocvm.c </td>

<td> 54 </td>

</tr>

<tr>

<td> 0×0013 </td>

<td> NtApphelpCacheControl </td>

</tr>

<tr>

<td> 0×0014 </td>

<td> NtAreMappedFilesTheSame </td>

<td> base/ntos/mm/mapview.c </td>

<td> 4357 </td>

</tr>

<tr>

<td> 0×0015 </td>

<td> NtAssignProcessToJobObject </td>

<td> base/ntos/ps/psjob.c </td>

<td> 267 </td>

</tr>

<tr>

<td> 0×0016 </td>

<td> NtCallbackReturn </td>

<td> base/ntos/ke/i386/callout.asm </td>

<td> 400 </td>

</tr>

<tr>

<td> 0×0017 </td>

<td> NtCancelDeviceWakeupRequest </td>

</tr>

<tr>

<td> 0×0018 </td>

<td> NtCancelIoFile </td>

<td> base/ntos/io/iomgr/misc.c </td>

<td> 40 </td>

</tr>

<tr>

<td> 0×0019 </td>

<td> NtCancelTimer </td>

<td> base/ntos/ex/timer.c </td>

<td> 710 </td>

</tr>

<tr>

<td> 0×001A </td>

<td> NtClearEvent </td>

<td> base/ntos/ex/event.c </td>

<td> 125 </td>

</tr>

<tr>

<td> 0×001B </td>

<td> NtClose </td>

<td> base/ntos/ob/obclose.c </td>

<td> 399 </td>

</tr>

<tr>

<td> 0×001C </td>

<td> NtCloseObjectAuditAlarm </td>

<td> base/ntos/se/seaudit.c </td>

<td> 2468 </td>

</tr>

<tr>

<td> 0×001D </td>

<td> NtCompactKeys </td>

<td> base/ntos/config/ntapi.c </td>

<td> 5248 </td>

</tr>

<tr>

<td> 0×001E </td>

<td> NtCompareTokens </td>

<td> base/ntos/se/token.c </td>

<td> 3951 </td>

</tr>

<tr>

<td> 0×001F </td>

<td> NtCompleteConnectPort </td>

<td> base/ntos/lpc/lpccompl.c </td>

<td> 865 </td>

</tr>

<tr>

<td> 0×0020 </td>

<td> NtCompressKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 5438 </td>

</tr>

<tr>

<td> 0×0021 </td>

<td> NtConnectPort </td>

<td> base/ntos/lpc/lpcconn.c </td>

<td> 42 </td>

</tr>

<tr>

<td> 0×0022 </td>

<td> NtContinue </td>

<td> base/ntos/ke/i386/trap.asm </td>

<td> 6534 </td>

</tr>

<tr>

<td> 0×0023 </td>

<td> NtCreateDebugObject </td>

<td> base/ntos/dbgk/dbgkobj.c </td>

<td> 458 </td>

</tr>

<tr>

<td> 0×0024 </td>

<td> NtCreateDirectoryObject </td>

<td> base/ntos/ob/obdir.c </td>

<td> 145 </td>

</tr>

<tr>

<td> 0×0025 </td>

<td> NtCreateEvent </td>

<td> base/ntos/ex/event.c </td>

<td> 180 </td>

</tr>

<tr>

<td> 0×0026 </td>

<td> NtCreateEventPair </td>

<td> base/ntos/ex/eventpr.c </td>

<td> 121 </td>

</tr>

<tr>

<td> 0×0027 </td>

<td> NtCreateFile </td>

<td> base/ntos/io/iomgr/create.c </td>

<td> 28 </td>

</tr>

<tr>

<td> 0×0028 </td>

<td> NtCreateIoCompletion </td>

<td> base/ntos/io/iomgr/complete.c </td>

<td> 45 </td>

</tr>

<tr>

<td> 0×0029 </td>

<td> NtCreateJobObject </td>

<td> base/ntos/ps/psjob.c </td>

<td> 73 </td>

</tr>

<tr>

<td> 0×002A </td>

<td> NtCreateJobSet </td>

<td> base/ntos/ps/psjob.c </td>

<td> 3260 </td>

</tr>

<tr>

<td> 0×002B </td>

<td> NtCreateKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 132 </td>

</tr>

<tr>

<td> 0×002C </td>

<td> NtCreateMailslotFile </td>

<td> base/ntos/io/iomgr/create.c </td>

<td> 276 </td>

</tr>

<tr>

<td> 0×002D </td>

<td> NtCreateMutant </td>

<td> base/ntos/ex/mutant.c </td>

<td> 152 </td>

</tr>

<tr>

<td> 0×002E </td>

<td> NtCreateNamedPipeFile </td>

<td> base/ntos/io/iomgr/create.c </td>

<td> 116 </td>

</tr>

<tr>

<td> 0×002F </td>

<td> NtCreatePagingFile </td>

<td> base/ntos/mm/modwrite.c </td>

<td> 329 </td>

</tr>

<tr>

<td> 0×0030 </td>

<td> NtCreatePort </td>

<td> base/ntos/lpc/lpccreat.c </td>

<td> 43 </td>

</tr>

<tr>

<td> 0×0031 </td>

<td> NtCreateProcess </td>

<td> base/ntos/ps/create.c </td>

<td> 816 </td>

</tr>

<tr>

<td> 0×0032 </td>

<td> NtCreateProcessEx </td>

<td> base/ntos/ps/create.c </td>

<td> 853 </td>

</tr>

<tr>

<td> 0×0033 </td>

<td> NtCreateProfile </td>

<td> base/ntos/ex/profile.c </td>

<td> 204 </td>

</tr>

<tr>

<td> 0×0034 </td>

<td> NtCreateSection </td>

<td> base/ntos/mm/creasect.c </td>

<td> 132 </td>

</tr>

<tr>

<td> 0×0035 </td>

<td> NtCreateSemaphore </td>

<td> base/ntos/ex/semphore.c </td>

<td> 121 </td>

</tr>

<tr>

<td> 0×0036 </td>

<td> NtCreateSymbolicLinkObject </td>

<td> base/ntos/ob/oblink.c </td>

<td> 57 </td>

</tr>

<tr>

<td> 0×0037 </td>

<td> NtCreateThread </td>

<td> base/ntos/ps/create.c </td>

<td> 78 </td>

</tr>

<tr>

<td> 0×0038 </td>

<td> NtCreateTimer </td>

<td> base/ntos/ex/timer.c </td>

<td> 488 </td>

</tr>

<tr>

<td> 0×0039 </td>

<td> NtCreateToken </td>

<td> base/ntos/se/token.c </td>

<td> 1934 </td>

</tr>

<tr>

<td> 0×003A </td>

<td> NtCreateWaitablePort </td>

<td> base/ntos/lpc/lpccreat.c </td>

<td> 85 </td>

</tr>

<tr>

<td> 0×003B </td>

<td> NtDebugActiveProcess </td>

<td> base/ntos/dbgk/dbgkobj.c </td>

<td> 1457 </td>

</tr>

<tr>

<td> 0×003C </td>

<td> NtDebugContinue </td>

<td> base/ntos/dbgk/dbgkobj.c </td>

<td> 2010 </td>

</tr>

<tr>

<td> 0×003D </td>

<td> NtDelayExecution </td>

<td> base/ntos/ex/delay.c </td>

<td> 24 </td>

</tr>

<tr>

<td> 0×003E </td>

<td> NtDeleteAtom </td>

<td> base/ntos/ex/exatom.c </td>

<td> 263 </td>

</tr>

<tr>

<td> 0×003F </td>

<td> NtDeleteBootEntry </td>

</tr>

<tr>

<td> 0×0040 </td>

<td> NtDeleteDriverEntry </td>

</tr>

<tr>

<td> 0×0041 </td>

<td> NtDeleteFile </td>

<td> base/ntos/io/iomgr/misc.c </td>

<td> 291 </td>

</tr>

<tr>

<td> 0×0042 </td>

<td> NtDeleteKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 392 </td>

</tr>

<tr>

<td> 0×0043 </td>

<td> NtDeleteObjectAuditAlarm </td>

<td> base/ntos/se/seaudit.c </td>

<td> 2598 </td>

</tr>

<tr>

<td> 0×0044 </td>

<td> NtDeleteValueKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 499 </td>

</tr>

<tr>

<td> 0×0045 </td>

<td> NtDeviceIoControlFile </td>

<td> base/ntos/io/iomgr/devctrl.c </td>

<td> 25 </td>

</tr>

<tr>

<td> 0×0046 </td>

<td> NtDisplayString </td>

</tr>

<tr>

<td> 0×0047 </td>

<td> NtDuplicateObject </td>

<td> base/ntos/ob/obhandle.c </td>

<td> 727 </td>

</tr>

<tr>

<td> 0×0048 </td>

<td> NtDuplicateToken </td>

<td> base/ntos/se/tokendup.c </td>

<td> 39 </td>

</tr>

<tr>

<td> 0×0049 </td>

<td> NtEnumerateBootEntries </td>

</tr>

<tr>

<td> 0×004A </td>

<td> NtEnumerateDriverEntries </td>

</tr>

<tr>

<td> 0×004B </td>

<td> NtEnumerateKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 624 </td>

</tr>

<tr>

<td> 0×004C </td>

<td> NtEnumerateSystemEnvironmentValuesEx </td>

</tr>

<tr>

<td> 0×004D </td>

<td> NtEnumerateValueKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 786 </td>

</tr>

<tr>

<td> 0×004E </td>

<td> NtExtendSection </td>

<td> base/ntos/mm/extsect.c </td>

<td> 86 </td>

</tr>

<tr>

<td> 0×004F </td>

<td> NtFilterToken </td>

<td> base/ntos/se/tokendup.c </td>

<td> 1365 </td>

</tr>

<tr>

<td> 0×0050 </td>

<td> NtFindAtom </td>

<td> base/ntos/ex/exatom.c </td>

<td> 158 </td>

</tr>

<tr>

<td> 0×0051 </td>

<td> NtFlushBuffersFile </td>

<td> base/ntos/io/iomgr/misc.c </td>

<td> 380 </td>

</tr>

<tr>

<td> 0×0052 </td>

<td> NtFlushInstructionCache </td>

<td> base/ntos/mm/flushbuf.c </td>

<td> 149 </td>

</tr>

<tr>

<td> 0×0053 </td>

<td> NtFlushKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 950 </td>

</tr>

<tr>

<td> 0×0054 </td>

<td> NtFlushVirtualMemory </td>

<td> base/ntos/mm/flushsec.c </td>

<td> 43 </td>

</tr>

<tr>

<td> 0×0055 </td>

<td> NtFlushWriteBuffer </td>

<td> base/ntos/mm/flushbuf.c </td>

<td> 39 </td>

</tr>

<tr>

<td> 0×0056 </td>

<td> NtFreeUserPhysicalPages </td>

<td> base/ntos/mm/physical.c </td>

<td> 2013 </td>

</tr>

<tr>

<td> 0×0057 </td>

<td> NtFreeVirtualMemory </td>

<td> base/ntos/mm/freevm.c </td>

<td> 42 </td>

</tr>

<tr>

<td> 0×0058 </td>

<td> NtFsControlFile </td>

<td> base/ntos/io/iomgr/fsctrl.c </td>

<td> 25 </td>

</tr>

<tr>

<td> 0×0059 </td>

<td> NtGetContextThread </td>

<td> base/ntos/ps/psctx.c </td>

<td> 309 </td>

</tr>

<tr>

<td> 0×005A </td>

<td> NtGetDevicePowerState </td>

</tr>

<tr>

<td> 0×005B </td>

<td> NtGetPlugPlayEvent </td>

</tr>

<tr>

<td> 0×005C </td>

<td> NtGetWriteWatch </td>

<td> base/ntos/mm/wrtwatch.c </td>

<td> 25 </td>

</tr>

<tr>

<td> 0×005D </td>

<td> NtImpersonateAnonymousToken </td>

<td> base/ntos/se/token.c </td>

<td> 3584 </td>

</tr>

<tr>

<td> 0×005E </td>

<td> NtImpersonateClientOfPort </td>

<td> base/ntos/lpc/lpcpriv.c </td>

<td> 29 </td>

</tr>

<tr>

<td> 0×005F </td>

<td> NtImpersonateThread </td>

<td> base/ntos/ps/psimpers.c </td>

<td> 27 </td>

</tr>

<tr>

<td> 0×0060 </td>

<td> NtInitializeRegistry </td>

<td> base/ntos/config/ntapi.c </td>

<td> 1030 </td>

</tr>

<tr>

<td> 0×0061 </td>

<td> NtInitiatePowerAction </td>

</tr>

<tr>

<td> 0×0062 </td>

<td> NtIsProcessInJob </td>

<td> base/ntos/ps/psjob.c </td>

<td> 3117 </td>

</tr>

<tr>

<td> 0×0063 </td>

<td> NtIsSystemResumeAutomatic </td>

</tr>

<tr>

<td> 0×0064 </td>

<td> NtListenPort </td>

<td> base/ntos/lpc/lpclistn.c </td>

<td> 27 </td>

</tr>

<tr>

<td> 0×0065 </td>

<td> NtLoadDriver </td>

<td> base/ntos/io/iomgr/loadunld.c </td>

<td> 27 </td>

</tr>

<tr>

<td> 0×0066 </td>

<td> NtLoadKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 3159 </td>

</tr>

<tr>

<td> 0×0067 </td>

<td> NtLoadKey2 </td>

<td> base/ntos/config/ntapi.c </td>

<td> 3207 </td>

</tr>

<tr>

<td> 0×0068 </td>

<td> NtLoadKeyEx </td>

<td> base/ntos/config/ntapi.c </td>

<td> 3260 </td>

</tr>

<tr>

<td> 0×0069 </td>

<td> NtLockFile </td>

<td> base/ntos/io/iomgr/lock.c </td>

<td> 26 </td>

</tr>

<tr>

<td> 0×006A </td>

<td> NtLockProductActivationKeys </td>

</tr>

<tr>

<td> 0×006B </td>

<td> NtLockRegistryKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 5510 </td>

</tr>

<tr>

<td> 0×006C </td>

<td> NtLockVirtualMemory </td>

<td> base/ntos/mm/lockvm.c </td>

<td> 24 </td>

</tr>

<tr>

<td> 0×006D </td>

<td> NtMakePermanentObject </td>

<td> base/ntos/ob/obdir.c </td>

<td> 2881 </td>

</tr>

<tr>

<td> 0×006E </td>

<td> NtMakeTemporaryObject </td>

<td> base/ntos/ob/obclose.c </td>

<td> 425 </td>

</tr>

<tr>

<td> 0×006F </td>

<td> NtMapUserPhysicalPages </td>

<td> base/ntos/mm/physical.c </td>

<td> 118 </td>

</tr>

<tr>

<td> 0×0070 </td>

<td> NtMapUserPhysicalPagesScatter </td>

<td> base/ntos/mm/physical.c </td>

<td> 633 </td>

</tr>

<tr>

<td> 0×0071 </td>

<td> NtMapViewOfSection </td>

<td> base/ntos/mm/mapview.c </td>

<td> 181 </td>

</tr>

<tr>

<td> 0×0072 </td>

<td> NtModifyBootEntry </td>

</tr>

<tr>

<td> 0×0073 </td>

<td> NtModifyDriverEntry </td>

</tr>

<tr>

<td> 0×0074 </td>

<td> NtNotifyChangeDirectoryFile </td>

<td> base/ntos/io/iomgr/dir.c </td>

<td> 859 </td>

</tr>

<tr>

<td> 0×0075 </td>

<td> NtNotifyChangeKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 1219 </td>

</tr>

<tr>

<td> 0×0076 </td>

<td> NtNotifyChangeMultipleKeys </td>

<td> base/ntos/config/ntapi.c </td>

<td> 1375 </td>

</tr>

<tr>

<td> 0×0077 </td>

<td> NtOpenDirectoryObject </td>

<td> base/ntos/ob/obdir.c </td>

<td> 259 </td>

</tr>

<tr>

<td> 0×0078 </td>

<td> NtOpenEvent </td>

<td> base/ntos/ex/event.c </td>

<td> 305 </td>

</tr>

<tr>

<td> 0×0079 </td>

<td> NtOpenEventPair </td>

<td> base/ntos/ex/eventpr.c </td>

<td> 233 </td>

</tr>

<tr>

<td> 0×007A </td>

<td> NtOpenFile </td>

<td> base/ntos/io/iomgr/open.c </td>

<td> 25 </td>

</tr>

<tr>

<td> 0×007B </td>

<td> NtOpenIoCompletion </td>

<td> base/ntos/io/iomgr/complete.c </td>

<td> 172 </td>

</tr>

<tr>

<td> 0×007C </td>

<td> NtOpenJobObject </td>

<td> base/ntos/ps/psjob.c </td>

<td> 191 </td>

</tr>

<tr>

<td> 0×007D </td>

<td> NtOpenKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 2028 </td>

</tr>

<tr>

<td> 0×007E </td>

<td> NtOpenMutant </td>

<td> base/ntos/ex/mutant.c </td>

<td> 272 </td>

</tr>

<tr>

<td> 0×007F </td>

<td> NtOpenObjectAuditAlarm </td>

<td> base/ntos/se/seaudit.c </td>

<td> 2054 </td>

</tr>

<tr>

<td> 0×0080 </td>

<td> NtOpenProcess </td>

<td> base/ntos/ps/psopen.c </td>

<td> 28 </td>

</tr>

<tr>

<td> 0×0081 </td>

<td> NtOpenProcessToken </td>

<td> base/ntos/se/tokenopn.c </td>

<td> 182 </td>

</tr>

<tr>

<td> 0×0082 </td>

<td> NtOpenProcessTokenEx </td>

<td> base/ntos/se/tokenopn.c </td>

<td> 220 </td>

</tr>

<tr>

<td> 0×0083 </td>

<td> NtOpenSection </td>

<td> base/ntos/mm/creasect.c </td>

<td> 4982 </td>

</tr>

<tr>

<td> 0×0084 </td>

<td> NtOpenSemaphore </td>

<td> base/ntos/ex/semphore.c </td>

<td> 252 </td>

</tr>

<tr>

<td> 0×0085 </td>

<td> NtOpenSymbolicLinkObject </td>

<td> base/ntos/ob/oblink.c </td>

<td> 246 </td>

</tr>

<tr>

<td> 0×0086 </td>

<td> NtOpenThread </td>

<td> base/ntos/ps/psopen.c </td>

<td> 272 </td>

</tr>

<tr>

<td> 0×0087 </td>

<td> NtOpenThreadToken </td>

<td> base/ntos/se/tokenopn.c </td>

<td> 489 </td>

</tr>

<tr>

<td> 0×0088 </td>

<td> NtOpenThreadTokenEx </td>

<td> base/ntos/se/tokenopn.c </td>

<td> 551 </td>

</tr>

<tr>

<td> 0×0089 </td>

<td> NtOpenTimer </td>

<td> base/ntos/ex/timer.c </td>

<td> 620 </td>

</tr>

<tr>

<td> 0×008A </td>

<td> NtPlugPlayControl </td>

</tr>

<tr>

<td> 0×008B </td>

<td> NtPowerInformation </td>

</tr>

<tr>

<td> 0×008C </td>

<td> NtPrivilegeCheck </td>

<td> base/ntos/se/privileg.c </td>

<td> 228 </td>

</tr>

<tr>

<td> 0×008D </td>

<td> NtPrivilegeObjectAuditAlarm </td>

<td> base/ntos/se/seaudit.c </td>

<td> 407 </td>

</tr>

<tr>

<td> 0×008E </td>

<td> NtPrivilegedServiceAuditAlarm </td>

<td> base/ntos/se/seaudit.c </td>

<td> 709 </td>

</tr>

<tr>

<td> 0×008F </td>

<td> NtProtectVirtualMemory </td>

<td> base/ntos/mm/protect.c </td>

<td> 50 </td>

</tr>

<tr>

<td> 0×0090 </td>

<td> NtPulseEvent </td>

<td> base/ntos/ex/event.c </td>

<td> 395 </td>

</tr>

<tr>

<td> 0×0091 </td>

<td> NtQueryAttributesFile </td>

<td> base/ntos/io/iomgr/misc.c </td>

<td> 625 </td>

</tr>

<tr>

<td> 0×0092 </td>

<td> NtQueryBootEntryOrder </td>

</tr>

<tr>

<td> 0×0093 </td>

<td> NtQueryBootOptions </td>

</tr>

<tr>

<td> 0×0094 </td>

<td> NtQueryDebugFilterState </td>

</tr>

<tr>

<td> 0×0095 </td>

<td> NtQueryDefaultLocale </td>

<td> base/ntos/ex/sysinfo.c </td>

<td> 465 </td>

</tr>

<tr>

<td> 0×0096 </td>

<td> NtQueryDefaultUILanguage </td>

<td> base/ntos/ex/sysinfo.c </td>

<td> 696 </td>

</tr>

<tr>

<td> 0×0097 </td>

<td> NtQueryDirectoryFile </td>

<td> base/ntos/io/iomgr/dir.c </td>

<td> 716 </td>

</tr>

<tr>

<td> 0×0098 </td>

<td> NtQueryDirectoryObject </td>

<td> base/ntos/ob/obdir.c </td>

<td> 343 </td>

</tr>

<tr>

<td> 0×0099 </td>

<td> NtQueryDriverEntryOrder </td>

</tr>

<tr>

<td> 0×009A </td>

<td> NtQueryEaFile </td>

<td> base/ntos/io/iomgr/qsea.c </td>

<td> 26 </td>

</tr>

<tr>

<td> 0×009B </td>

<td> NtQueryEvent </td>

<td> base/ntos/ex/event.c </td>

<td> 489 </td>

</tr>

<tr>

<td> 0×009C </td>

<td> NtQueryFullAttributesFile </td>

<td> base/ntos/io/iomgr/misc.c </td>

<td> 749 </td>

</tr>

<tr>

<td> 0×009D </td>

<td> NtQueryInformationAtom </td>

<td> base/ntos/ex/exatom.c </td>

<td> 301 </td>

</tr>

<tr>

<td> 0×009E </td>

<td> NtQueryInformationFile </td>

<td> base/ntos/io/iomgr/qsinfo.c </td>

<td> 91 </td>

</tr>

<tr>

<td> 0×009F </td>

<td> NtQueryInformationJobObject </td>

<td> base/ntos/ps/psjob.c </td>

<td> 904 </td>

</tr>

<tr>

<td> 0×00A0 </td>

<td> NtQueryInformationPort </td>

<td> base/ntos/lpc/lpcquery.c </td>

<td> 28 </td>

</tr>

<tr>

<td> 0×00A1 </td>

<td> NtQueryInformationProcess </td>

<td> base/ntos/ps/psquery.c </td>

<td> 590 </td>

</tr>

<tr>

<td> 0×00A2 </td>

<td> NtQueryInformationThread </td>

<td> base/ntos/ps/psquery.c </td>

<td> 3041 </td>

</tr>

<tr>

<td> 0×00A3 </td>

<td> NtQueryInformationToken </td>

<td> base/ntos/se/tokenqry.c </td>

<td> 34 </td>

</tr>

<tr>

<td> 0×00A4 </td>

<td> NtQueryInstallUILanguage </td>

<td> base/ntos/ex/sysinfo.c </td>

<td> 665 </td>

</tr>

<tr>

<td> 0×00A5 </td>

<td> NtQueryIntervalProfile </td>

<td> base/ntos/ex/profile.c </td>

<td> 757 </td>

</tr>

<tr>

<td> 0×00A6 </td>

<td> NtQueryIoCompletion </td>

<td> base/ntos/io/iomgr/complete.c </td>

<td> 275 </td>

</tr>

<tr>

<td> 0×00A7 </td>

<td> NtQueryKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 2189 </td>

</tr>

<tr>

<td> 0×00A8 </td>

<td> NtQueryMultipleValueKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 4191 </td>

</tr>

<tr>

<td> 0×00A9 </td>

<td> NtQueryMutant </td>

<td> base/ntos/ex/mutant.c </td>

<td> 368 </td>

</tr>

<tr>

<td> 0×00AA </td>

<td> NtQueryObject </td>

<td> base/ntos/ob/obquery.c </td>

<td> 53 </td>

</tr>

<tr>

<td> 0×00AB </td>

<td> NtQueryOpenSubKeys </td>

<td> base/ntos/config/ntapi.c </td>

<td> 4750 </td>

</tr>

<tr>

<td> 0×00AC </td>

<td> NtQueryOpenSubKeysEx </td>

<td> base/ntos/config/ntapi.c </td>

<td> 4905 </td>

</tr>

<tr>

<td> 0×00AD </td>

<td> NtQueryPerformanceCounter </td>

<td> base/ntos/ex/profile.c </td>

<td> 821 </td>

</tr>

<tr>

<td> 0×00AE </td>

<td> NtQueryQuotaInformationFile </td>

<td> base/ntos/io/iomgr/qsquota.c </td>

<td> 26 </td>

</tr>

<tr>

<td> 0×00AF </td>

<td> NtQuerySection </td>

<td> base/ntos/mm/querysec.c </td>

<td> 28 </td>

</tr>

<tr>

<td> 0×00B0 </td>

<td> NtQuerySecurityObject </td>

<td> base/ntos/ob/obse.c </td>

<td> 251 </td>

</tr>

<tr>

<td> 0×00B1 </td>

<td> NtQuerySemaphore </td>

<td> base/ntos/ex/semphore.c </td>

<td> 343 </td>

</tr>

<tr>

<td> 0×00B2 </td>

<td> NtQuerySymbolicLinkObject </td>

<td> base/ntos/ob/oblink.c </td>

<td> 331 </td>

</tr>

<tr>

<td> 0×00B3 </td>

<td> NtQuerySystemEnvironmentValue </td>

</tr>

<tr>

<td> 0×00B4 </td>

<td> NtQuerySystemEnvironmentValueEx </td>

</tr>

<tr>

<td> 0×00B5 </td>

<td> NtQuerySystemInformation </td>

<td> base/ntos/ex/sysinfo.c </td>

<td> 1391 </td>

</tr>

<tr>

<td> 0×00B6 </td>

<td> NtQuerySystemTime </td>

</tr>

<tr>

<td> 0×00B7 </td>

<td> NtQueryTimer </td>

<td> base/ntos/ex/timer.c </td>

<td> 846 </td>

</tr>

<tr>

<td> 0×00B8 </td>

<td> NtQueryTimerResolution </td>

</tr>

<tr>

<td> 0×00B9 </td>

<td> NtQueryValueKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 2370 </td>

</tr>

<tr>

<td> 0×00BA </td>

<td> NtQueryVirtualMemory </td>

<td> base/ntos/mm/queryvm.c </td>

<td> 39 </td>

</tr>

<tr>

<td> 0×00BB </td>

<td> NtQueryVolumeInformationFile </td>

<td> base/ntos/io/iomgr/qsfs.c </td>

<td> 28 </td>

</tr>

<tr>

<td> 0×00BC </td>

<td> NtQueueApcThread </td>

<td> base/ntos/ps/psctx.c </td>

<td> 61 </td>

</tr>

<tr>

<td> 0×00BD </td>

<td> NtRaiseException </td>

<td> base/ntos/ke/i386/trap.asm </td>

<td> 6622 </td>

</tr>

<tr>

<td> 0×00BE </td>

<td> NtRaiseHardError </td>

<td> base/ntos/ex/harderr.c </td>

<td> 606 </td>

</tr>

<tr>

<td> 0×00BF </td>

<td> NtReadFile </td>

<td> base/ntos/io/iomgr/read.c </td>

<td> 31 </td>

</tr>

<tr>

<td> 0×00C0 </td>

<td> NtReadFileScatter </td>

<td> base/ntos/io/iomgr/read.c </td>

<td> 737 </td>

</tr>

<tr>

<td> 0×00C1 </td>

<td> NtReadRequestData </td>

<td> base/ntos/lpc/lpcreply.c </td>

<td> 870 </td>

</tr>

<tr>

<td> 0×00C2 </td>

<td> NtReadVirtualMemory </td>

<td> base/ntos/mm/readwrt.c </td>

<td> 92 </td>

</tr>

<tr>

<td> 0×00C3 </td>

<td> NtRegisterThreadTerminatePort </td>

<td> base/ntos/ps/psdelete.c </td>

<td> 1679 </td>

</tr>

<tr>

<td> 0×00C4 </td>

<td> NtReleaseMutant </td>

<td> base/ntos/ex/mutant.c </td>

<td> 505 </td>

</tr>

<tr>

<td> 0×00C5 </td>

<td> NtReleaseSemaphore </td>

<td> base/ntos/ex/semphore.c </td>

<td> 476 </td>

</tr>

<tr>

<td> 0×00C6 </td>

<td> NtRemoveIoCompletion </td>

<td> base/ntos/io/iomgr/complete.c </td>

<td> 479 </td>

</tr>

<tr>

<td> 0×00C7 </td>

<td> NtRemoveProcessDebug </td>

<td> base/ntos/dbgk/dbgkobj.c </td>

<td> 1548 </td>

</tr>

<tr>

<td> 0×00C8 </td>

<td> NtRenameKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 5084 </td>

</tr>

<tr>

<td> 0×00C9 </td>

<td> NtReplaceKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 4068 </td>

</tr>

<tr>

<td> 0×00CA </td>

<td> NtReplyPort </td>

<td> base/ntos/lpc/lpcreply.c </td>

<td> 59 </td>

</tr>

<tr>

<td> 0×00CB </td>

<td> NtReplyWaitReceivePort </td>

<td> base/ntos/lpc/lpcrecv.c </td>

<td> 28 </td>

</tr>

<tr>

<td> 0×00CC </td>

<td> NtReplyWaitReceivePortEx </td>

<td> base/ntos/lpc/lpcrecv.c </td>

<td> 102 </td>

</tr>

<tr>

<td> 0×00CD </td>

<td> NtReplyWaitReplyPort </td>

<td> base/ntos/lpc/lpcreply.c </td>

<td> 399 </td>

</tr>

<tr>

<td> 0×00CE </td>

<td> NtRequestDeviceWakeup </td>

</tr>

<tr>

<td> 0×00CF </td>

<td> NtRequestPort </td>

<td> base/ntos/lpc/lpcsend.c </td>

<td> 41 </td>

</tr>

<tr>

<td> 0×00D0 </td>

<td> NtRequestWaitReplyPort </td>

<td> base/ntos/lpc/lpcsend.c </td>

<td> 430 </td>

</tr>

<tr>

<td> 0×00D1 </td>

<td> NtRequestWakeupLatency </td>

</tr>

<tr>

<td> 0×00D2 </td>

<td> NtResetEvent </td>

<td> base/ntos/ex/event.c </td>

<td> 620 </td>

</tr>

<tr>

<td> 0×00D3 </td>

<td> NtResetWriteWatch </td>

<td> base/ntos/mm/wrtwatch.c </td>

<td> 607 </td>

</tr>

<tr>

<td> 0×00D4 </td>

<td> NtRestoreKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 2555 </td>

</tr>

<tr>

<td> 0×00D5 </td>

<td> NtResumeProcess </td>

<td> base/ntos/ps/psspnd.c </td>

<td> 441 </td>

</tr>

<tr>

<td> 0×00D6 </td>

<td> NtResumeThread </td>

<td> base/ntos/ps/psspnd.c </td>

<td> 323 </td>

</tr>

<tr>

<td> 0×00D7 </td>

<td> NtSaveKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 2679 </td>

</tr>

<tr>

<td> 0×00D8 </td>

<td> NtSaveKeyEx </td>

<td> base/ntos/config/ntapi.c </td>

<td> 2764 </td>

</tr>

<tr>

<td> 0×00D9 </td>

<td> NtSaveMergedKeys </td>

<td> base/ntos/config/ntapi.c </td>

<td> 2871 </td>

</tr>

<tr>

<td> 0×00DA </td>

<td> NtSecureConnectPort </td>

<td> base/ntos/lpc/lpcconn.c </td>

<td> 83 </td>

</tr>

<tr>

<td> 0×00DB </td>

<td> NtSetBootEntryOrder </td>

</tr>

<tr>

<td> 0×00DC </td>

<td> NtSetBootOptions </td>

</tr>

<tr>

<td> 0×00DD </td>

<td> NtSetContextThread </td>

<td> base/ntos/ps/psctx.c </td>

<td> 529 </td>

</tr>

<tr>

<td> 0×00DE </td>

<td> NtSetDebugFilterState </td>

</tr>

<tr>

<td> 0×00DF </td>

<td> NtSetDefaultHardErrorPort </td>

<td> base/ntos/ex/harderr.c </td>

<td> 918 </td>

</tr>

<tr>

<td> 0×00E0 </td>

<td> NtSetDefaultLocale </td>

<td> base/ntos/ex/sysinfo.c </td>

<td> 502 </td>

</tr>

<tr>

<td> 0×00E1 </td>

<td> NtSetDefaultUILanguage </td>

<td> base/ntos/ex/sysinfo.c </td>

<td> 962 </td>

</tr>

<tr>

<td> 0×00E2 </td>

<td> NtSetDriverEntryOrder </td>

</tr>

<tr>

<td> 0×00E3 </td>

<td> NtSetEaFile </td>

<td> base/ntos/io/iomgr/qsea.c </td>

<td> 645 </td>

</tr>

<tr>

<td> 0×00E4 </td>

<td> NtSetEvent </td>

<td> base/ntos/ex/event.c </td>

<td> 712 </td>

</tr>

<tr>

<td> 0×00E5 </td>

<td> NtSetEventBoostPriority </td>

<td> base/ntos/ex/event.c </td>

<td> 800 </td>

</tr>

<tr>

<td> 0×00E6 </td>

<td> NtSetHighEventPair </td>

<td> base/ntos/ex/eventpr.c </td>

<td> 621 </td>

</tr>

<tr>

<td> 0×00E7 </td>

<td> NtSetHighWaitLowEventPair </td>

<td> base/ntos/ex/eventpr.c </td>

<td> 504 </td>

</tr>

<tr>

<td> 0×00E8 </td>

<td> NtSetInformationDebugObject </td>

<td> base/ntos/dbgk/dbgkobj.c </td>

<td> 2126 </td>

</tr>

<tr>

<td> 0×00E9 </td>

<td> NtSetInformationFile </td>

<td> base/ntos/io/iomgr/qsinfo.c </td>

<td> 836 </td>

</tr>

<tr>

<td> 0×00EA </td>

<td> NtSetInformationJobObject </td>

<td> base/ntos/ps/psjob.c </td>

<td> 1444 </td>

</tr>

<tr>

<td> 0×00EB </td>

<td> NtSetInformationKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 3894 </td>

</tr>

<tr>

<td> 0×00EC </td>

<td> NtSetInformationObject </td>

<td> base/ntos/ob/obquery.c </td>

<td> 657 </td>

</tr>

<tr>

<td> 0×00ED </td>

<td> NtSetInformationProcess </td>

<td> base/ntos/ps/psquery.c </td>

<td> 1981 </td>

</tr>

<tr>

<td> 0×00EE </td>

<td> NtSetInformationThread </td>

<td> base/ntos/ps/psquery.c </td>

<td> 3503 </td>

</tr>

<tr>

<td> 0×00EF </td>

<td> NtSetInformationToken </td>

<td> base/ntos/se/tokenset.c </td>

<td> 38 </td>

</tr>

<tr>

<td> 0×00F0 </td>

<td> NtSetIntervalProfile </td>

<td> base/ntos/ex/profile.c </td>

<td> 730 </td>

</tr>

<tr>

<td> 0×00F1 </td>

<td> NtSetIoCompletion </td>

<td> base/ntos/io/iomgr/complete.c </td>

<td> 411 </td>

</tr>

<tr>

<td> 0×00F2 </td>

<td> NtSetLdtEntries </td>

<td> base/ntos/ps/i386/psldt.c </td>

<td> 1465 </td>

</tr>

<tr>

<td> 0×00F3 </td>

<td> NtSetLowEventPair </td>

<td> base/ntos/ex/eventpr.c </td>

<td> 563 </td>

</tr>

<tr>

<td> 0×00F4 </td>

<td> NtSetLowWaitHighEventPair </td>

<td> base/ntos/ex/eventpr.c </td>

<td> 445 </td>

</tr>

<tr>

<td> 0×00F5 </td>

<td> NtSetQuotaInformationFile </td>

<td> base/ntos/io/iomgr/qsquota.c </td>

<td> 609 </td>

</tr>

<tr>

<td> 0×00F6 </td>

<td> NtSetSecurityObject </td>

<td> base/ntos/ob/obse.c </td>

<td> 44 </td>

</tr>

<tr>

<td> 0×00F7 </td>

<td> NtSetSystemEnvironmentValue </td>

</tr>

<tr>

<td> 0×00F8 </td>

<td> NtSetSystemEnvironmentValueEx </td>

</tr>

<tr>

<td> 0×00F9 </td>

<td> NtSetSystemInformation </td>

<td> base/ntos/ex/sysinfo.c </td>

<td> 3068 </td>

</tr>

<tr>

<td> 0×00FA </td>

<td> NtSetSystemPowerState </td>

</tr>

<tr>

<td> 0×00FB </td>

<td> NtSetSystemTime </td>

</tr>

<tr>

<td> 0×00FC </td>

<td> NtSetThreadExecutionState </td>

</tr>

<tr>

<td> 0×00FD </td>

<td> NtSetTimer </td>

<td> base/ntos/ex/timer.c </td>

<td> 981 </td>

</tr>

<tr>

<td> 0×00FE </td>

<td> NtSetTimerResolution </td>

</tr>

<tr>

<td> 0×00FF </td>

<td> NtSetUuidSeed </td>

<td> base/ntos/ex/uuid.c </td>

<td> 541 </td>

</tr>

<tr>

<td> 0×0100 </td>

<td> NtSetValueKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 2976 </td>

</tr>

<tr>

<td> 0×0101 </td>

<td> NtSetVolumeInformationFile </td>

<td> base/ntos/io/iomgr/qsfs.c </td>

<td> 534 </td>

</tr>

<tr>

<td> 0×0102 </td>

<td> NtShutdownSystem </td>

<td> base/ntos/ex/exinit.c </td>

<td> 460 </td>

</tr>

<tr>

<td> 0×0103 </td>

<td> NtSignalAndWaitForSingleObject </td>

<td> base/ntos/ob/obwait.c </td>

<td> 45 </td>

</tr>

<tr>

<td> 0×0104 </td>

<td> NtStartProfile </td>

<td> base/ntos/ex/profile.c </td>

<td> 499 </td>

</tr>

<tr>

<td> 0×0105 </td>

<td> NtStopProfile </td>

<td> base/ntos/ex/profile.c </td>

<td> 651 </td>

</tr>

<tr>

<td> 0×0106 </td>

<td> NtSuspendProcess </td>

<td> base/ntos/ps/psspnd.c </td>

<td> 398 </td>

</tr>

<tr>

<td> 0×0107 </td>

<td> NtSuspendThread </td>

<td> base/ntos/ps/psspnd.c </td>

<td> 206 </td>

</tr>

<tr>

<td> 0×0108 </td>

<td> NtSystemDebugControl </td>

</tr>

<tr>

<td> 0×0109 </td>

<td> NtTerminateJobObject </td>

<td> base/ntos/ps/psjob.c </td>

<td> 2412 </td>

</tr>

<tr>

<td> 0×010A </td>

<td> NtTerminateProcess </td>

<td> base/ntos/ps/psdelete.c </td>

<td> 274 </td>

</tr>

<tr>

<td> 0×010B </td>

<td> NtTerminateThread </td>

<td> base/ntos/ps/psdelete.c </td>

<td> 528 </td>

</tr>

<tr>

<td> 0×010C </td>

<td> NtTestAlert </td>

<td> base/ntos/ps/psspnd.c </td>

<td> 611 </td>

</tr>

<tr>

<td> 0×010D </td>

<td> NtTraceEvent </td>

<td> base/ntos/wmi/traceapi.c </td>

<td> 1034 </td>

</tr>

<tr>

<td> 0×010E </td>

<td> NtTranslateFilePath </td>

</tr>

<tr>

<td> 0×010F </td>

<td> NtUnloadDriver </td>

<td> base/ntos/io/iomgr/loadunld.c </td>

<td> 247 </td>

</tr>

<tr>

<td> 0×0110 </td>

<td> NtUnloadKey </td>

<td> base/ntos/config/ntapi.c </td>

<td> 3466 </td>

</tr>

<tr>

<td> 0×0111 </td>

<td> NtUnloadKey2 </td>

<td> base/ntos/config/ntapi.c </td>

<td> 3504 </td>

</tr>

<tr>

<td> 0×0112 </td>

<td> NtUnloadKeyEx </td>

<td> base/ntos/config/ntapi.c </td>

<td> 3710 </td>

</tr>

<tr>

<td> 0×0113 </td>

<td> NtUnlockFile </td>

<td> base/ntos/io/iomgr/lock.c </td>

<td> 475 </td>

</tr>

<tr>

<td> 0×0114 </td>

<td> NtUnlockVirtualMemory </td>

<td> base/ntos/mm/lockvm.c </td>

<td> 571 </td>

</tr>

<tr>

<td> 0×0115 </td>

<td> NtUnmapViewOfSection </td>

<td> base/ntos/mm/umapview.c </td>

<td> 29 </td>

</tr>

<tr>

<td> 0×0116 </td>

<td> NtVdmControl </td>

</tr>

<tr>

<td> 0×0117 </td>

<td> NtWaitForDebugEvent </td>

<td> base/ntos/dbgk/dbgkobj.c </td>

<td> 1812 </td>

</tr>

<tr>

<td> 0×0118 </td>

<td> NtWaitForMultipleObjects </td>

<td> base/ntos/ob/obwait.c </td>

<td> 422 </td>

</tr>

<tr>

<td> 0×0119 </td>

<td> NtWaitForSingleObject </td>

<td> base/ntos/ob/obwait.c </td>

<td> 296 </td>

</tr>

<tr>

<td> 0×011A </td>

<td> NtWaitHighEventPair </td>

<td> base/ntos/ex/eventpr.c </td>

<td> 385 </td>

</tr>

<tr>

<td> 0×011B </td>

<td> NtWaitLowEventPair </td>

<td> base/ntos/ex/eventpr.c </td>

<td> 325 </td>

</tr>

<tr>

<td> 0×011C </td>

<td> NtWriteFile </td>

<td> base/ntos/io/iomgr/write.c </td>

<td> 25 </td>

</tr>

<tr>

<td> 0×011D </td>

<td> NtWriteFileGather </td>

<td> base/ntos/io/iomgr/write.c </td>

<td> 788 </td>

</tr>

<tr>

<td> 0×011E </td>

<td> NtWriteRequestData </td>

<td> base/ntos/lpc/lpcreply.c </td>

<td> 927 </td>

</tr>

<tr>

<td> 0×011F </td>

<td> NtWriteVirtualMemory </td>

<td> base/ntos/mm/readwrt.c </td>

<td> 226 </td>

</tr>

<tr>

<td> 0×0120 </td>

<td> NtYieldExecution </td>

<td> base/ntos/ke/yield.c </td>

<td> 23 </td>

</tr>

<tr>

<td> 0×0121 </td>

<td> NtCreateKeyedEvent </td>

<td> base/ntos/ex/keyedevent.c </td>

<td> 198 </td>

</tr>

<tr>

<td> 0×0122 </td>

<td> NtOpenKeyedEvent </td>

<td> base/ntos/ex/keyedevent.c </td>

<td> 309 </td>

</tr>

<tr>

<td> 0×0123 </td>

<td> NtReleaseKeyedEvent </td>

<td> base/ntos/ex/keyedevent.c </td>

<td> 383 </td>

</tr>

<tr>

<td> 0×0124 </td>

<td> NtWaitForKeyedEvent </td>

<td> base/ntos/ex/keyedevent.c </td>

<td> 552 </td>

</tr>

<tr>

<td> 0×0125 </td>

<td> NtQueryPortInformationProcess </td>

<td> base/ntos/ps/psquery.c </td>

<td> 1668 </td>

</tr>

<tr>

<td> 0×0126 </td>

<td> NtGetCurrentProcessorNumber </td>

<td> base/ntos/ps/psquery.c </td>

<td> 4214 </td>

</tr>

<tr>

<td> 0×0127 </td>

<td> NtWaitForMultipleObjects32 </td>

<td> base/ntos/ob/obwait.c </td>

<td> 519 </td>

</tr>

</tbody>

</table>

* * *