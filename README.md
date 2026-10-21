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
1) Device discovery (DVPiper -listdevicexml      List all available devices in XML format) so that DV Scheduler can add devices
2) tune to frewquency and scan for channels so that DV Scheduler can add channels
3) tune to frequency and read the epg: DVPiper.exe -devicenum %d -type DVB-T -frequency %d -bandwidth 7 -epg output_file.xml
4) tune to frequency and record program to file reporting statistics (error rates packet/other) for recording
Note that there can be overlapping recordings initiated through the same dvpiper instance via command through stdin/stdout.
