# CBT495
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. GitHub repos will be deleted and created during this period...

```
//***FILE 495 is Tom Conley's Dynamic ISPF Starter Set (DISS), a    *   FILE 495
//*           set of REXX execs to dynamically allocate datasets    *   FILE 495
//*           necessary to run the ISPF interfaces of many common   *   FILE 495
//*           software packages.  This collection of sample execs   *   FILE 495
//*           was designed to make it easier to install these       *   FILE 495
//*           ISPF interfaces, without adding DD names to your      *   FILE 495
//*           installation's LOGON PROCs.  Lots of samples here!    *   FILE 495
//*           Email:  pinncons@rochester.rr.com                     *   FILE 495
//*                                                                 *   FILE 495
//* Dynamic ISPF is a methodology to eliminate ISPF datasets from   *   FILE 495
//* TSO logon procs by using the dynamic allocation functions of    *   FILE 495
//* ISPF and TSO to allocate ISPF application datasets instead.     *   FILE 495
//* For more information about Dynamic ISPF, please visit           *   FILE 495
//* http://home.rochester.rr.com/pinncons and download Tom Conley's *   FILE 495
//* Dynamic ISPF SHARE presentation.                                *   FILE 495
//*                                                                 *   FILE 495
//* This starter set includes REXX execs to invoke many standard    *   FILE 495
//* ISPF applications.  If you have any problems, suggestions, or   *   FILE 495
//* to contribute an exec of your own, please Email Tom Conley at   *   FILE 495
//* pinncons@rochester.rr.com.  This exec library will be updated   *   FILE 495
//* periodically and posted at http://www.cbttape.org and           *   FILE 495
//* http://home.roadrunner.com/~pinncons                            *   FILE 495
//*                                                                 *   FILE 495
//* In order to understand and install the varied components of     *   FILE 495
//* the Dynamic ISPF Starter Set, refer to the following members:   *   FILE 495
//*                                                                 *   FILE 495
//*  $CHANGES - Change log of all changes to DISS                   *   FILE 495
//*  $INSTALL - Installation instructions for each release          *   FILE 495
//*  $README  - Starting point for DISS                             *   FILE 495
//*  $READWAC - Documentation and installation instructions for     *   FILE 495
//*             World According to Conley (WAC) ISPF method         *   FILE 495
//*                                                                 *   FILE 495
//* The following list of members is followed by a short            *   FILE 495
//* description to show you the ISPF applications supported by the  *   FILE 495
//* Dynamic ISPF Starter Set:                                       *   FILE 495
//*                                                                 *   FILE 495
//*  $BOOKINS - Installation instructions for BookManager support   *   FILE 495
//*  $CHANGES - Change log of all changes to DISS                   *   FILE 495
//*  $DYNDTL  - Example showing how to invoke DISS apps from DTL    *   FILE 495
//*  $DYNDT12 - DTL example for z/OS V1R2 and higher                *   FILE 495
//*  $DYNMENU - Menu to invoke Dynamic ISPF REXX execs              *   FILE 495
//*  $FILE495 - This member                                         *   FILE 495
//*  $INSTALL - Installation instructions for each release          *   FILE 495
//*  $README  - Starting point for DISS                             *   FILE 495
//*  $READWAC - Documentation for WAC ISPF method                   *   FILE 495
//*  @$AVRS   - SEA's $AVRS                                         *   FILE 495
//*  @ABNDAID - Compuware's AbendAid                                *   FILE 495
//*  @ACF2    - CA's ACF2                                           *   FILE 495
//*  @AMDSADD - IBM's StandAlone Dump Dataset Initialization EXEC   *   FILE 495
//*  @APA     - IBM's Application Performance Analyzer              *   FILE 495
//*  @APPC    - IBM's APPC administration                           *   FILE 495
//*  @ASM2    - CA's ASM2                                           *   FILE 495
//*  @ASTEX   - CA's ASTEX                                          *   FILE 495
//*  @ASU     - IBM's DCE Application Support                       *   FILE 495
//*  @AXCIS   - Kodak's AXCIS                                       *   FILE 495
//*  @BDT     - IBM's Bulk Data Transfer                            *   FILE 495
//*  @BOOKBLD - IBM's BookManager BUILD                             *   FILE 495
//*  @BOOKDBC - IBM's BookManager DBCS Print                        *   FILE 495
//*  @BOOKIND - IBM's BookManager INDEX                             *   FILE 495
//*  @BOOKRED - IBM's BookManager READ                              *   FILE 495
//*  @CADISK  - CA's DISK                                           *   FILE 495
//*  @CALIBR  - CA's LIBRARIAN                                      *   FILE 495
//*  @CAOPERA - CA's OPERA                                          *   FILE 495
//*  @CAOPT   - CA's Optimizer                                      *   FILE 495
//*  @CASPOOL - CA's SPOOL                                          *   FILE 495
//*  @CATLMS  - CA's TLMS                                           *   FILE 495
//*  @CATSS   - CA's Top Secret                                     *   FILE 495
//*  @CAVTAPE - CA's VTAPE                                          *   FILE 495
//*  @CAXCOM  - CA's XCOM                                           *   FILE 495
//*  @CA1     - CA's CA-1 Tape Management System                    *   FILE 495
//*  @CA11    - CA's CA-11 Job Restart System                       *   FILE 495
//*  @CA7     - CA's CA-7 Job Control System                        *   FILE 495
//*  @CICMEU1 - IBM's CICS Message Editing Utility                  *   FILE 495
//*  @CICMEU2 - IBM's CICS Message Editing Utility                  *   FILE 495
//*  @COMMAND - MACRO4's COMMAND                                    *   FILE 495
//*  @COMPARX - Serena's COMPAREX                                   *   FILE 495
//*  @CPSM    - IBM's CICSPlex System Manager                       *   FILE 495
//*  @CTLGSOL - Softworks's Catalog Solution                        *   FILE 495
//*  @CWLMA   - Compuware License Management                        *   FILE 495
//*  @CWUTILS - Compuware Utilities                                 *   FILE 495
//*  @DB2ADM  - IBM's DB2 Administrator                             *   FILE 495
//*  @DB2I    - IBM's DB2 Interactive                               *   FILE 495
//*  @DCECONF - IBM's DCE Configuration                             *   FILE 495
//*  @DELIVER - CA's DELIVER                                        *   FILE 495
//*  @DFSCONF - IBM's Distributed File Service Configuration        *   FILE 495
//*  @DFSORT  - IBM's DF/SORT                                       *   FILE 495
//*  @DITTO   - IBM's DITTO                                         *   FILE 495
//*  @DMPMSTI - MACRO4's DUMPMASTER Installation                    *   FILE 495
//*  @DMPMSTR - MACRO4's DUMPMASTER                                 *   FILE 495
//*  @EJES    - Phoenix Software International's (E)JES             *   FILE 495
//*  @ENDEVOR - CA's ENDEVOR Change Control                         *   FILE 495
//*  @EPILOG  - Candle's EPILOG/MVS                                 *   FILE 495
//*  @ESP     - Cybermation's @ESP                                  *   FILE 495
//*  @ETFACF2 - Eberhard Klemens ETF ACF2                           *   FILE 495
//*  @ETFRACF - Eberhard Klemens ETF RACF                           *   FILE 495
//*  @EXAMINE - CA's EXAMINE                                        *   FILE 495
//*  @FAT     - Innovation's FATS/FATAR                             *   FILE 495
//*  @FAULTAN - IBM's FaultAnalyzer                                 *   FILE 495
//*  @FDRABR  - Innovation's FDR/ABR                                *   FILE 495
//*  @FFST    - IBM's First Failure Support Technology              *   FILE 495
//*  @FILEAID - Compuware's FILEAID                                 *   FILE 495
//*  @FILEIMS - Compuware's FILEAID/IMS                             *   FILE 495
//*  @FIMGRV1 - IBM's FileManager Version 1                         *   FILE 495
//*  @FIMGRV2 - IBM's FileManager Version 2                         *   FILE 495
//*  @GDDMPQM - IBM's GDDM Print Queue Manager                      *   FILE 495
//*  @GRSMON  - IBM's GRS Monitor                                   *   FILE 495
//*  @GRSMON1 - IBM's GRS Monitor Stub                              *   FILE 495
//*  @HCD     - IBM's Hardware Configuration                        *   FILE 495
//*  @IAM     - Innovation's Innovation Access Method               *   FILE 495
//*  @ICSF    - IBM's Integrated Cryptographic Services Facility    *   FILE 495
//*  @IEF     - CA's IEF                                            *   FILE 495
//*  @IMOD    - CA's IMOD editor for GSS                            *   FILE 495
//*  @INFOCTR - IBM's TSO/E Informtion Center                       *   FILE 495
//*  @INFOPRT - IBM's InfoPrint                                     *   FILE 495
//*  @IOF     - Triangle Systems' Interactive Output Facility       *   FILE 495
//*  @IPCS    - IBM's Interactive Problem Control System            *   FILE 495
//*  @IPCSIM1 - IBM's IPCS with IMS support                         *   FILE 495
//*  @IPCSIM2 - IBM's IPCS with IMS support                         *   FILE 495
//*  @IPCSJ2  - IBM's IPCS with JES2 support                        *   FILE 495
//*  @IPCSJ3  - IBM's IPCS with JES3 support                        *   FILE 495
//*  @IPCSMNU - IBM's IPCS main menu exec enables submenu options   *   FILE 495
//*  @IPCSTC1 - IBM's IPCS with TCP/IP support                      *   FILE 495
//*  @IPCSTC2 - IBM's IPCS with TCP/IP support                      *   FILE 495
//*  @ISHELL  - IBM's ISPF Shell for Unix System Services           *   FILE 495
//*  @ISM     - CA's Integrated Storage Mangement                   *   FILE 495
//*  @ISMF    - IBM's Interactive Storage Mangement Facility        *   FILE 495
//*  @ISPCONF - IBM's ISPF Configuration                            *   FILE 495
//*  @ISRV    - CA's ISERVE for GSS                                 *   FILE 495
//*  @IXFP    - IBM's (Storage Tek's) Extended Facilities Product   *   FILE 495
//*  @JCLCHEK - CA's JCLCHECK                                       *   FILE 495
//*  @JESMSTR - Xenos' JES-Master Spool Viewer                      *   FILE 495
//*  @JOBTRAC - CA's JOBTRAC Job Tracking System                    *   FILE 495
//*  @LANRES  - IBM's LANRES                                        *   FILE 495
//*  @LOGRECV - IBM's LOGREC Viewer                                 *   FILE 495
//*  @MQSRIES - IBM's MQSeries Administration Stub                  *   FILE 495
//*  @MQSRS52 - IBM's MQSeries Administration V5R2 and earlier      *   FILE 495
//*  @MQSRS53 - IBM's MQSeries Administration V5R3 and later        *   FILE 495
//*  @MXI     - Rob Scott's MXI                                     *   FILE 495
//*  @NDM     - Sterling's Connect:Direct (NDM)                     *   FILE 495
//*  @NETVFTP - IBM's NetView FTP                                   *   FILE 495
//*  @NPF     - IBM's Network Print Facility                        *   FILE 495
//*  @OBROWSE - IBM's OpenMVS Browse                                *   FILE 495
//*  @OEDIT   - IBM's OpenMVS Edit                                  *   FILE 495
//*  @OMEGCIC - Candle's OMEGAMON/CICS                              *   FILE 495
//*  @OMEGMVS - Candle's OMEGAMON/MVS                               *   FILE 495
//*  @OMVS    - IBM's OpenMVS Command Processor                     *   FILE 495
//*  @OPC     - IBM's Operations Planning and Control               *   FILE 495
//*  @OPCINST - IBM's Operations Planning and Control Installation  *   FILE 495
//*  @OPSBRW  - CA's OPS/MVS OPSLOG Browse                          *   FILE 495
//*  @OPSMVS  - CA's OPS/MVS                                        *   FILE 495
//*  @OSA     - IBM's Open Systems Adapter Configuration            *   FILE 495
//*  @PANAPT  - CA's PANAPT                                         *   FILE 495
//*  @PANVLET - CA's PANVALET                                       *   FILE 495
//*  @PDS     - PDS Freeware from CBT Tape File 182                 *   FILE 495
//*  @PDSMAN  - CA's PDSMAN                                         *   FILE 495
//*  @PERFSOL - Softworks's Performance Solution                    *   FILE 495
//*  @PLATDBT - Platinum's DBTools                                  *   FILE 495
//*  @PLP     - Lionel Dyck's Product Launch Point                  *   FILE 495
//*  @PRMTOOL - IBM's PARMLIB Tool                                  *   FILE 495
//*  @PROSMS  - BMC's ProSMS                                        *   FILE 495
//*  @QABATCH - Compuware's QABatch                                 *   FILE 495
//*  @QMF     - IBM's Query Management Facility for DB2             *   FILE 495
//*  @QMFOLD  - IBM's Query Management Facility for DB2 V6+         *   FILE 495
//*  @QWIKREF - ChicagoSoft's QuickRef                              *   FILE 495
//*  @RACF    - IBM's Resource Access Control Facility              *   FILE 495
//*  @RA2     - SEA's RA2 RACF Management                           *   FILE 495
//*  @RESOLVE - BMC's RESOLVE                                       *   FILE 495
//*  @RMDS    - IBM's Report Management Distribution System         *   FILE 495
//*  @RMDSOLM - IBM's RMDS Online Management                        *   FILE 495
//*  @RMF     - IBM's Resource Management Facility                  *   FILE 495
//*  @RMM     - IBM's Removable Media Manager                       *   FILE 495
//*  @RRS     - IBM's RRS                                           *   FILE 495
//*  @SAADMIN - IBM's System Automation ADMIN                       *   FILE 495
//*  @SAIOCON - IBM's System Automation IOCONNECT                   *   FILE 495
//*  @SASC    - SAS/C Compiler                                      *   FILE 495
//*  @SCLM    - IBM's Software Configuration Library Manager        *   FILE 495
//*  @SDSF    - IBM's Spool Display & Search Facility               *   FILE 495
//*  @SDSF1   - IBM's Spool Display & Search Facility               *   FILE 495
//*  @SERVPAC - IBM's ServerPac Installation                        *   FILE 495
//*  @SMPE    - IBM's System Modification Program / Extended        *   FILE 495
//*  @SOMOBJS - IBM's SOMObjects Compiler                           *   FILE 495
//*  @STROBE  - Compuware's STROBE                                  *   FILE 495
//*  @SUNRISE - Amdahl's SUNRISE                                    *   FILE 495
//*  @SVAA    - Sun's Shared Virtual Array Administrator            *   FILE 495
//*  @SYNCINT - SyncSort Installation                               *   FILE 495
//*  @SYNCMSG - SyncSort Messages                                   *   FILE 495
//*  @SYSVIEW - CA's SYSVIEW/E                                      *   FILE 495
//*  @TABLBAS - DataKinetics tableBase                              *   FILE 495
//*  @TAPRCLM - OpenTech's Tape Reclaim                             *   FILE 495
//*  @TASID   - Doug Nadel's TASID (separate load and panel libs)   *   FILE 495
//*  @TASID0  - Doug Nadel's TASID (single load module)             *   FILE 495
//*  @TDMF    - SofTek's Transparent Data Migrtion Facility         *   FILE 495
//*  @TSOMON  - CA's TSOMON                                         *   FILE 495
//*  @UPSTREM - Innovation's Upstream                               *   FILE 495
//*  @VANGARD - Vanguard RACF Administration                        *   FILE 495
//*  @VIACENT - VIASOFT's VIA/CENTER                                *   FILE 495
//*  @VIEW    - CA's View (SAR)                                     *   FILE 495
//*  @VIEWDIR - Mobius's ViewDirect                                 *   FILE 495
//*  @VMCF    - LRS's VPS Monitor and Control Facility              *   FILE 495
//*  @VPSPRNT - LRS's VPSPRINT                                      *   FILE 495
//*  @VSAMMEC - Catalog Solutions VSAM MECHANIC                     *   FILE 495
//*  @VTAMDMP - IBM's VTAM Dump Analysis IPCS                       *   FILE 495
//*  @VTAMDM1 - IBM's VTAM Dump Analysis IPCS Stub                  *   FILE 495
//*  @VTAMTRC - IBM's VTAM Trace Analysis IPCS                      *   FILE 495
//*  @VTAMTR1 - IBM's VTAM Trace Analysis IPCS Stub                 *   FILE 495
//*  @WLM     - IBM's Workload Manager                              *   FILE 495
//*  @XDC     - Cole Software's XDC                                 *   FILE 495
//*  @XMITIP  - Lionel Dyck's XMITIP Email                          *   FILE 495
//*  @XPATH   - Xerox's XPATH                                       *   FILE 495
//*  @ZEKE    - Allen Systems's ZEKE/ZEBB                           *   FILE 495
//*  ABRALLOC - Innovation's FDR/ABR                                *   FILE 495
//*  ALLUSER  - WAC sample of company-wide menu for all users       *   FILE 495
//*  BOOKMGR  - Alias for EOXBKMGR                                  *   FILE 495
//*  C11IEXEC - CA's CA-11                                          *   FILE 495
//*  DSNECPRI - IBM DB2I CLIST (modified for DISS)                  *   FILE 495
//*  EOXBKMGR - IBM BookManager exec (modified for DISS)            *   FILE 495
//*  EOXREDIT - IBM BookManager exec (modified for DISS)            *   FILE 495
//*  EOXVHELP - IBM BookManager exec (modified for DISS)            *   FILE 495
//*  ERBRMFX  - IBM RMF CLIST (modified for DISS)                   *   FILE 495
//*  ERB0PRM  - IBM RMF Primary Option Menu (modified for DISS)     *   FILE 495
//*  EZBDCMDS - Command table member for TCP/IP IPCS                *   FILE 495
//*  IKJTSO00 - WAC sample of TSO PARMLIB member for HELP datasets  *   FILE 495
//*  ISMPANL  - CA's ISM option menu modified with PASSLIB, SCRNAME *   FILE 495
//*  ISR@PRIM - WAC sample of Primary Option Menu with A&Z options  *   FILE 495
//*  ISR@PUL2 - DTL include with ZSEL code for $DYNDTL to compile   *   FILE 495
//*  JCKSPF   - CA's JCLCHECK                                       *   FILE 495
//*  OY59638  - IBM APAR showing why LOGON should always be CLIST   *   FILE 495
//*  PERSISPF - WAC sample of EXEC for a personal ISPF environment  *   FILE 495
//*  SHAREDOC - Dynamic ISPF SHARE presentation MSWord binary image *   FILE 495
//*  TBPRIM   - DataKinetics' tablesONLINE menu (modified for DISS) *   FILE 495
//*  TSOAPPL  - WAC sample of TSO LOGON PROC for Applications       *   FILE 495
//*  TSOAPPL# - WAC sample of ISPF selection menu for Applications  *   FILE 495
//*  TSOLOGON - WAC sample of LOGON CLIST                           *   FILE 495
//*  TSOSYSP  - WAC sample of TSO LOGON PROC for SysProgs           *   FILE 495
//*  TSOSYSP# - WAC sample of ISPF selection menu for SysProgs      *   FILE 495
//*  UMISPFP  - WAC sample of ISPF usermod for ISR@PRIM             *   FILE 495
//*                                                                 *   FILE 495
```
