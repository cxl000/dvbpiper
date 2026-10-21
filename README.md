This prject is develop a drop in replacement for DVPiper.exe as used by DV Scheduler, a Java based TV recording tool.
The replacement should be able to be run on Windows BDA devices and Linuc DVB devices.

Initial target is to support DVB-T devices to tune to Australia/Melbourne channels.
HSV6    177500kHz
SBS7    184500kHz
GTV8    191625kHz
ATV11   219500kHz
ABC12   226500kHz
MGV32   557625kHz

This is used by a Java based TV recording tool: DV Scheduler.
It should support DV Scheduler functions

1. Device discovery: uses command line arguments: (DVPiper -listdevicexml      List all available devices in XML format) so that DV Scheduler can add devices
2. tune to frequency and scan for channels so that DV Scheduler can add channel. Uses command argumnets to tume (DVPiper.exe" -windowscodepage -epgmintime 30000 -epgmaxtime 420000 -forceexit -minclean 0.1 -tuning 1 -log "C:\\ProgramData\\DV Scheduler\\log\\DVPiper\_2026-1
3. 0-21.log" -devicename2 @device:pnp:\\\\?\\usb#vid\_2040\&pid\_8265#0014232710#{71985f48-1ca1-11d3-9cc8-00c04f7971e0}\\{510162d9-2f7e-49e7-907b-dbd3a5a15eb9} -type DVB-T -frequency 177500 -modulation " " -symbolrate -2 -phychannel -2 -bandwidth 7
4. &#x20;-polar " " -osc1 -2 -osc2 -2 -lnbswitch -2 -longitude -2.0 -dirlongitude Unknown -azimuth -2.0 -elevation -2.0 -inputrange " " -pilot " " -roll-off " " -fec " " -diseqc " " -diseqcwait -2 -charset " " -scanmaxtime 60000 -provmaxtime 6000
5. 0 -udpsockbuffer 65536 -httpsockbuffer 65536 -postdelay 0
6. ) and input commands: signal
 scan(file('$scanFilename'),rid($rid),complete,strict,tsfiledec('$encUtf8UrlScanTsFilename'))
7. tune to frequency and read the epg: DVPiper.exe -devicenum %d -type DVB-T -frequency %d -bandwidth 7 -epg output\_file.xml
8. tune to frequency and record program to file reporting statistics (error rates packet/other) for recording
Note that there can be overlapping recordings initiated through the same dvpiper instance via command through stdin/stdout.

