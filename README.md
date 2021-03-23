# cms-opendata-validation
Test of *2011-jet-inclusivecrosssection-ntupleproduction* codes  
## Host System properties
Intel Core i3-8130 CPU@ 2.20 GHz 2.20 GHz, 4 GB RAM, 64 Bit, Windows 10 Pro
## Virtual Machine  
CMS-OpenData-1.5.2 on Oracle VirtualBox-6.1.12 
## 2011-jet-inclusivecrosssection-ntupleproduction
For this example informations are available [here](https://github.com/cms-opendata-validation/2011-jet-inclusivecrosssection-ntupleproduction)
## Code testing status
Initially, Oracle VirtualBox-6.1.12 installed on a labtop then CMS-OpenData-1.5.2 used as a operating system. If everything goes fine your Virtual Machine screen looks like this 

![image](https://user-images.githubusercontent.com/66729789/111881100-1e4cae00-89c0-11eb-8a3d-937c8d18170a.png). 

To test codes open `CMS S...` therminal. Everything goes fine till `Run the program` section. To run the .py file for data with cmsRun `CMS Shell > cmsRun OpenDataTreeProducerOptimized_dataPAT_2011_cfg.py`. It gives error message which is 

````html 
CMS Shell > cmsRun OpenDataTreeProducerOptimized_dataPAT_2011_cfg.py 
%MSG-w LocalFileSystem::initFSList():  (NoModuleName) 20-Mar-2021 21:27:17 +03  pre-events
Cannot read '/etc/mtab': Invalid argument (error 22)
%MSG
CORAL/RelationalPlugins/sqlite Error SQLiteStatement::fetchNext 1 SQL logic error or missing database
CORAL/RelationalPlugins/sqlite Error SQLiteStatement::finalize 10 disk I/O error
CORAL/RelationalPlugins/sqlite Error SQLiteStatement::finalize 1 cannot commit - no transaction is active
CORAL/RelationalPlugins/sqlite Error SQLiteStatement::execute 1 cannot commit - no transaction is active
----- Begin Fatal Exception 20-Mar-2021 21:34:44 +03-----------------------
An exception of category 'StdException' occurred while
   [0] Constructing the EventProcessor
   [1] Constructing ESSource: class=PoolDBESSource label='GlobalTag'
Exception Message:
A std::exception was thrown.
cannot commit - no transaction is active ( CORAL : "SQLiteStatement::execute" from "CORAL/RelationalPlugins/sqlite" )
----- End Fatal Exception -------------------------------------------------` 
````

For Monte Carlo data one error message seen but events counting

`CMS Shell > cmsRun OpenDataTreeProducerOptimized_mcPAT_2011_cfg.py
%MSG-w LocalFileSystem::initFSList():  (NoModuleName) 20-Mar-2021 21:44:41 +03  pre-events
Cannot read '/etc/mtab': Invalid argument (error 22)
%MSG
20-Mar-2021 21:47:18 +03  Initiating request to open file root://eospublic.cern.ch//eos/opendata/cms/MonteCarlo2011/Summer11LegDR/QCD_Pt-80to120_TuneZ2_7TeV_pythia6/AODSIM/PU_S13_START53_LV6-v1/00000/005D4394-1FB7-E311-91F4-002590593878.root
20-Mar-2021 21:47:21 +03  Successfully opened file root://eospublic.cern.ch//eos/opendata/cms/MonteCarlo2011/Summer11LegDR/QCD_Pt-80to120_TuneZ2_7TeV_pythia6/AODSIM/PU_S13_START53_LV6-v1/00000/005D4394-1FB7-E311-91F4-002590593878.root
Cross section: 784265 
* Begin processing the 1st record. Run 1, Event 10924, LumiSection 34 at 20-Mar-2021 21:48:08.388 +03 
* Begin processing the 501st record. Run 1, Event 14734, LumiSection 45 at 20-Mar-2021 21:49:28.722 +03 
* Begin processing the 1001st record. Run 1, Event 1138317, LumiSection 3440 at 20-Mar-2021 21:50:09.360 +03 
* Begin processing the 1501st record. Run 1, Event 1666762, LumiSection 5036 at 20-Mar-2021 21:50:42.610 +03 
* Begin processing the 2001st record. Run 1, Event 2260414, LumiSection 6830 at 20-Mar-2021 21:51:12.157 +03` 



